---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF41DDBA-6D4B-47A5-BCFF-3D0BB1D375C5
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2b6aaf5e8564b3eea675a57176b8f7118d2c7a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105960"
---
# <span data-ttu-id="61b01-101">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="61b01-101">Set-AzureHDInsightDefaultStorage</span></span>

## <span data-ttu-id="61b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61b01-102">SYNOPSIS</span></span>
<span data-ttu-id="61b01-103">HDInsight kümesi için varsayılan depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61b01-103">Sets the default storage account for an HDInsight cluster.</span></span>

## <span data-ttu-id="61b01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61b01-104">SYNTAX</span></span>

```
Set-AzureHDInsightDefaultStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> -StorageContainerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="61b01-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61b01-105">DESCRIPTION</span></span>
<span data-ttu-id="61b01-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="61b01-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="61b01-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="61b01-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="61b01-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="61b01-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="61b01-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="61b01-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="61b01-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="61b01-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="61b01-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="61b01-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="61b01-112">**Set-AzureHDInsightDefaultStorage** cmdlet 'i HDInsight küme yapılandırması için varsayılan depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61b01-112">The **Set-AzureHDInsightDefaultStorage** cmdlet sets the default storage account for an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="61b01-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61b01-113">EXAMPLES</span></span>

### <span data-ttu-id="61b01-114">Örnek 1: varsayılan depolama hesabını ayarlama</span><span class="sxs-lookup"><span data-stu-id="61b01-114">Example 1: Set the default storage account</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer"
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="61b01-115">İlk komut, geçerli abonelik KIMLIĞINI almak için **Get-Azuyeniden gönderme Scription** cmdlet 'ini kullanır ve ardından $SubId değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="61b01-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="61b01-116">İkinci ve üçüncü komutlar MyBlobStorage ve MySecondBlobStorage için birincil depolama anahtarlarını almak üzere **Get-AzureStorageKey** cmdlet 'ini kullanır ve ardından anahtarları $Key 1 ve $Key 2 değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="61b01-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="61b01-117">Dördüncü, beşinci ve altıncı komutlarıgeçerli aboneliğin kimlik bilgilerini almak için **Get-Credential** cmdlet 'ini kullanır ve sonra $Creds, $OozieCreds ve $HiveCreds değişkenlerinde kimlik bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="61b01-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription, and then stores the credentials in the $Creds, $OozieCreds, and $HiveCreds variables.</span></span>

<span data-ttu-id="61b01-118">Final komutu, aşağıdaki cmdlet 'leri kullanarak bir dizi işlemi gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="61b01-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="61b01-119">**New-AzureHDInsightClusterConfig-** HDInsight küme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61b01-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="61b01-120">**Set-AzureHDInsightDefaultStorage** , yapılandırmanın varsayılan depolama hesabını MyBlobStorage.blob.Core.Windows.net olarak ayarlamak için.</span><span class="sxs-lookup"><span data-stu-id="61b01-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="61b01-121">Yapılandırmaya MySecondBlobStorage.blob.core.windows.net adlı ikinci bir depolama hesabı eklemek için **Add-AzureHDInsightStorage** .</span><span class="sxs-lookup"><span data-stu-id="61b01-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="61b01-122">**Add-AzureHDInsightMetastore** , bir Oozie ve bir kovan için bir tam</span><span class="sxs-lookup"><span data-stu-id="61b01-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="61b01-123">Yeni **-AzureHDInsightCluster** yeni yapılandırmayla bir HDInsight kümesi oluşturmak için.</span><span class="sxs-lookup"><span data-stu-id="61b01-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="61b01-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61b01-124">PARAMETERS</span></span>

### <span data-ttu-id="61b01-125">-Config</span><span class="sxs-lookup"><span data-stu-id="61b01-125">-Config</span></span>
<span data-ttu-id="61b01-126">Yapılandırma nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61b01-126">Specifies a configuration object.</span></span>
<span data-ttu-id="61b01-127">Bu cmdlet, bu parametrenin belirttiği nesne için varsayılan depolama hesabını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61b01-127">This cmdlet sets the default storage account for the object that this parameter specifies.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61b01-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="61b01-128">-Profile</span></span>
<span data-ttu-id="61b01-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61b01-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61b01-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="61b01-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b01-131">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="61b01-131">-StorageAccountKey</span></span>
<span data-ttu-id="61b01-132">Varsayılan depolama hesabına erişmek için kullanılan depolama hesabı anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61b01-132">Specifies the storage account key that is used to access the default storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b01-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="61b01-133">-StorageAccountName</span></span>
<span data-ttu-id="61b01-134">Varsayılan depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61b01-134">Specifies the name of a default storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b01-135">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="61b01-135">-StorageContainerName</span></span>
<span data-ttu-id="61b01-136">Kümenin varsayılan depolama kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61b01-136">Specifies the name of the default storage container for a cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b01-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b01-137">CommonParameters</span></span>
<span data-ttu-id="61b01-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61b01-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b01-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b01-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b01-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61b01-140">INPUTS</span></span>

## <span data-ttu-id="61b01-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61b01-141">OUTPUTS</span></span>

## <span data-ttu-id="61b01-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61b01-142">NOTES</span></span>

## <span data-ttu-id="61b01-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61b01-143">RELATED LINKS</span></span>

[<span data-ttu-id="61b01-144">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="61b01-144">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="61b01-145">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="61b01-145">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="61b01-146">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="61b01-146">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="61b01-147">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="61b01-147">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


