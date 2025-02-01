def is_bullish_engulfing(candle1, candle2):
    return (candle1['close'] < candle1['open'] and  # Primeiro candle é de baixa
            candle2['close'] > candle2['open'] and  # Segundo candle é de alta
            candle2['close'] > candle1['open'] and  # Fecha acima da abertura do primeiro candle
            candle2['open'] < candle1['close'])  # Abre abaixo do fechamento do primeiro candle
            
