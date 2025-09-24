from keras.models import Model
from keras.layers import Input, LSTM, Dense, Embedding

# Define vocabulary sizes
num_encoder_tokens = 10000  # example value; replace with actual vocabulary size
num_decoder_tokens = 10000  # example value; replace with actual vocabulary size

# Define encoder
encoder_inputs = Input(shape=(None,), name='encoder_inputs')
enc_emb = Embedding(input_dim=num_encoder_tokens, output_dim=256, name='encoder_embedding')(encoder_inputs)
encoder_lstm, state_h, state_c = LSTM(256, return_state=True, name='encoder_lstm')(enc_emb)
encoder_states = [state_h, state_c]

# Define decoder
decoder_inputs = Input(shape=(None,), name='decoder_inputs')
dec_emb = Embedding(input_dim=num_decoder_tokens, output_dim=256, name='decoder_embedding')(decoder_inputs)
decoder_lstm = LSTM(256, return_sequences=True, return_state=True, name='decoder_lstm')
decoder_outputs, _, _ = decoder_lstm(dec_emb, initial_state=encoder_states)
decoder_dense = Dense(num_decoder_tokens, activation='softmax', name='decoder_dense')
decoder_outputs = decoder_dense(decoder_outputs)

# Define the model
model = Model([encoder_inputs, decoder_inputs], decoder_outputs)
model.compile(optimizer='rmsprop', loss='categorical_crossentropy', metrics=['accuracy'])

model.summary()
<img width="607" height="473" alt="Screenshot 2025-09-24 101317" src="https://github.com/user-attachments/assets/7b794a99-967c-4e74-a3c1-4a293d40471f" />
