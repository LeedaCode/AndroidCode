package com.example.smartcity.Override;

import android.text.method.PasswordTransformationMethod;
import android.util.Log;
import android.view.View;

import androidx.annotation.NonNull;

public class IDCardHide extends PasswordTransformationMethod {
    @Override
    public CharSequence getTransformation(CharSequence source, View view) {
        return new IDCardCharSequence(source);
    }
    private class  IDCardCharSequence implements CharSequence{
        private CharSequence mSource;
        public IDCardCharSequence(CharSequence source) {
            this.mSource = source;
        }

        @Override
        public int length() {
            return mSource.length();
        }

        @Override
        public char charAt(int i) {
            Log.i("Tag",i+"");
            if(i<2||i>length()-5){
                return mSource.charAt(i);
            }
            return '*';
        }

        @NonNull
        @Override
        public CharSequence subSequence(int i, int i1) {
            Log.i("Tag",i+","+i1);
             return mSource.subSequence(i,i1);
        }
    }
}
