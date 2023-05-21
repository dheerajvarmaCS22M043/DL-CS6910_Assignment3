# DL-CS6910_Assignment3
->My main files are A3_with_Atten (3).ipynb and A3_without_Attn (2).ipynb as those consist of model trained using hyperparameters and sweep runs are used to view those results

->prediction_vanilla (3).ipynb and Prediction_Attention.ipynb contain the results of test accuracy as well as code to generate .csv files which contian input, ground truth and output results

->prediction_vanilla.csv and prediction_Attention.csv files contains input, ground truth and output words of test dataset

->All the above .ipynb files can be executed on any python editor with gpu processor 

sweep_config = {

    "method": 'bayes', #grid, random
    
    "metric": {
    
      "name": 'validation_accuracy',
      
      "goal": 'maximize', 
      
    },
    
    "parameters": {
    
        "epochs": {
        
            "values": [15]
            
        },
        
        "dropout": {
        
            "values": [0.3,0.4,0.5]
            
        },
        
        "hidden_size": {
        
            "values": [128,256,512]
            
        },
        
        "embedding_size": {
        
            "values": [128,256,512]
            
        },
        
        "learning_rate":{
        
            "values":[0.001,0.05]
            
        },
        
        "batch_size":{
        
            "values":[32,64,128,256]
            
        },
        
        "num_layers":{
        
            "values":[1,3,2]
            
       },
       
        "bidirectional":{
        
            "values":[False,True]
            
        },
        
        "cell_type":{
        
            "values":['LSTM','RNN','GRU']
            
        }
        
    }
    
}

these are the my sweep parameters to train and experiment with model

-> my wandb report link: https://wandb.ai/cs22m043/Assignment_3_Report/reports/Report-CS6910-Assignment-3--Vmlldzo0NDIzNDM5
