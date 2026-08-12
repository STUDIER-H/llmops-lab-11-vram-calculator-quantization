# 🧪 LAB 11: Calculadora de Aritmética de Inferência VRAM (Kipply) & Quantização INT8/INT4

## 🎯 Objetivo do Lab
Aplicar a matemática do artigo de Kipply (*Transformer Inference Arithmetic*) para calcular a pegada de memória de LLMs e aplicar quantização em modelos reais.

---

## 📋 Pré-requisitos
- Ter lido o paper *Transformer Inference Arithmetic* (Kipply) e concluído *Deploying Deep Learning: Quantization* (Coursera).
- Python 3.10+, AutoAWQ / GPTQ / llama.cpp.

---

## 🛠️ O que você deve construir neste Lab:

### Etapa 1: Calculadora de VRAM (CLI Python)
1. Escreva uma CLI `vram_calc.py` que receba os parâmetros:
   - Número de parâmetros (ex: 8B).
   - Precisão (FP16, INT8, INT4).
   - Context Length (ex: 4096) e Batch Size (ex: 16).
2. O script deve calcular e retornar separadamente:
   - Memória dos Pesos (GB).
   - Memória do KV Cache (GB).
   - Diagnóstico se o workload é *Memory-bound* ou *Compute-bound*.

### Etapa 2: Quantização Prática
1. Converta o modelo Llama-3-8B de FP16 para INT4 usando AWQ ou GPTQ e compare a redução no footprint de VRAM.

---

## ✅ Critérios de Aceitação & Entrega
- [ ] CLI `vram_calc.py` calculando memória com precisão comprovada.
- [ ] Modelo quantizado rodando com redução de pelo menos 60% no consumo de VRAM.
