---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: 33e1e9ac0b62d378954280d8dd81361c0d075a1e
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2019
ms.locfileid: "93751012"
---
# Az. HDInsight modülü
## Tanım
Bu bölümdeki konular, Azure Resource Manager (ARM) çerçevesindeki Microsoft Azure HDInsight için Azure PowerShell cmdlet 'lerini belgeleyin. Bu cmdlet 'ler HDInsight kümelerini ve bunların üzerinde çalışan işleri yönetmek için kullanılır. Microsoft. Azure. Commands. HDInsight ad alanında cmdlet 'ler vardır.

## Az. HDInsight cmdlet 'Leri
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Küme yapılandırma nesnesine küme kimliği ekler.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Kümede çalışan bir hizmetin bir kopyasını küme yapılandırma nesnesine ekler.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Bir küme yapılandırma nesnesine bir Hadoop yapılandırma değeri özelleştirmesi ve/veya kovan Paylaşılan kitaplık özelleştirmesi ekler.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Bir SQL veritabanını yığın veya Oozie metaser olarak bir küme yapılandırma nesnesine ekler.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Küme yapılandırma nesnesine bir komut dosyası eylemi ekler.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Küme yapılandırma nesnesine güvenlik profili ekler.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Küme yapılandırma nesnesine Azure depolama anahtarı ekler.

### [Disable-AzHDInsightOperationsManagementSuite](Disable-AzHDInsightOperationsManagementSuite.md)
Bir HDInsight kümesindeki Operations Management paketini (OMS) devre dışı bırakır ve ilgili Günlükler, etkinleştir sırasında belirtilen OMS çalışma alanına akışını durdurur.

### [Enable-AzHDInsightOperationsManagementSuite](Enable-AzHDInsightOperationsManagementSuite.md)
Bir HDInsight kümesinde Operations Management Suite (OMS) özelliğini etkinleştirir ve ilgili Günlükler etkinleştir sırasında belirtilen OMS çalışma alanına gönderilir.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Geçerli abonelikle ilişkilendirilmiş tüm Azure HDInsight kümelerini veya belirli bir kaynak grubunu alır ve listeler.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Bir kümeden işlerin listesini alır ve bunları ters sırada listeler veya belirli bir iş alır.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Belirli bir kümeyle ilişkilendirilmiş depolama hesabından bir işin günlük çıkışını alır.

### [Get-AzHDInsightOperationsManagementSuite](Get-AzHDInsightOperationsManagementSuite.md)
Kümedeki Operations Management Suite (OMS) yüklemesinin durumunu alır.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Kümenin kalıcı komut dosyası eylemlerini alır ve bunları kronolojik sırada listeler veya belirli bir kalıcı betik eyleminin ayrıntılarını alır.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
HDInsight hizmeti hakkında, kullanılabilir konumlar ve kapasite gibi özellikleri alır.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Kümenin komut dosyası eylem geçmişini alır ve ters kronolojik sırayla listeler veya önceden çalıştırılmış bir betik eyleminin ayrıntılarını alır.

### [Grant-AzHDInsightRdpServicesAccess](Grant-AzHDInsightRdpServicesAccess.md)
Windows kümesine RDP erişimi verir.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Bir HDInsight kümesine kovan sorgusu gönderir ve sorgu sonuçlarını tek bir işlemde alır.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Geçerli abonelik için belirtilen kaynak grubunda bir Azure HDInsight kümesi oluşturur.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Azure HDInsight küme yapılandırmasını tanımlayan kalıcı olmayan bir küme yapılandırma nesnesi oluşturur.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Bir kovan iş nesnesi oluşturur.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
MapReduce iş nesnesi oluşturur.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Domuz iş nesnesi oluşturur.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Bir Sqoop iş nesnesi oluşturur.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Bir akış MapReduce iş nesnesi oluşturur.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Belirtilen HDInsight kümesini geçerli abonelikten kaldırır.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Bir HDInsight kümesinden kalıcı betik eylemini kaldırır.

### [Revoke-AzHDInsightRdpServicesAccess](Revoke-AzHDInsightRdpServicesAccess.md)
Windows kümesine RDP erişimini devre dışı bırakır.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Belirtilen kümede çalışan düğümü sayısını ayarlar.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Küme yapılandırma nesnesindeki varsayılan depolama hesabı ayarını ayarlar.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Azure HDInsight kümesinin ağ geçidi HTTP kimlik bilgilerini ayarlar.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Önceden çalıştırılmış bir betik eylemini kalıcı bir betik eylemi olarak ayarlar.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Belirtilen bir kümede tanımlı Azure HDInsight işini başlatır.

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
Kümede belirtilen çalışan işi durdurur.

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Bir Azure HDInsight kümesine yeni bir betik eylemi gönderir.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Invoke-RmAzureHDInsightHiveJob cmdlet 'inde kullanılacak kümeyi seçer.

### [Bekle-AzHDInsightJob](Wait-AzHDInsightJob.md)
Belirtilen işin tamamlanmasını veya başarısızlığını bekler.

