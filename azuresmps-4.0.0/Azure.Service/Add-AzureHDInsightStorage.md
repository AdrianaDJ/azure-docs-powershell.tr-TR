---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02435c28ca17666a3b19389fde039353f3d779a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105716"
---
# <span data-ttu-id="dc3cc-101">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="dc3cc-101">Add-AzureHDInsightStorage</span></span>

## <span data-ttu-id="dc3cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3cc-103">Bir HDInsight yapılandırmasına BLOB depolama hesabı girdisi ekler.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-103">Adds a blob storage account entry to an HDInsight configuration.</span></span>

## <span data-ttu-id="dc3cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc3cc-104">SYNTAX</span></span>

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dc3cc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc3cc-105">DESCRIPTION</span></span>
<span data-ttu-id="dc3cc-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="dc3cc-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="dc3cc-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="dc3cc-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="dc3cc-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="dc3cc-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="dc3cc-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="dc3cc-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dc3cc-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="dc3cc-112">**Add-AzureHDInsightStorage** cmdlet 'ı bir Azure HDInsight yapılandırmasına BLOB depolama hesabı girişi ekler.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-112">The **Add-AzureHDInsightStorage** cmdlet adds a blob storage account entry to an Azure HDInsight configuration.</span></span>

## <span data-ttu-id="dc3cc-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc3cc-113">EXAMPLES</span></span>

### <span data-ttu-id="dc3cc-114">Örnek 1: depolama hesabı ekleme</span><span class="sxs-lookup"><span data-stu-id="dc3cc-114">Example 1: Add a storage account</span></span>
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

<span data-ttu-id="dc3cc-115">Bu komut, $Config depolanan yapılandırma nesnesine MyStorage adlı bir depolama hesabı ekler ve sonra da yapılandırmayı $StoreConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-115">This command adds a storage account named MyStorage to the configuration object stored in $Config, and then stores the configuration in the $StoreConfig variable.</span></span>

### <span data-ttu-id="dc3cc-116">Örnek 2: birden çok depolama hesabını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="dc3cc-116">Example 2: Configure multiple storage accounts</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="dc3cc-117">İlk komut, geçerli abonelik KIMLIĞINI almak için **Get-Azuyeniden gönderme Scription** cmdlet 'ini kullanır ve ardından $SubId değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-117">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="dc3cc-118">İkinci ve üçüncü komutlar MyBlobStorage ve MySecondBlobStorage için birincil depolama anahtarlarını almak üzere **Get-AzureStorageKey** cmdlet 'ini kullanır ve ardından anahtarları $Key 1 ve $Key 2 değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-118">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="dc3cc-119">Dördüncü, beşinci ve altıncı komutları, geçerli aboneliğin ve Oozie ve kovan için kimlik bilgilerini alır ve ardından kimlik bilgilerini değişkenler halinde depolar.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-119">The fourth, fifth, and sixth commands get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="dc3cc-120">Final komutu, aşağıdaki cmdlet 'leri kullanarak bir dizi işlemi gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="dc3cc-120">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="dc3cc-121">**Yeni-AzureHDInsightClusterConfig** bir HDInsight küme yapılandırması oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="dc3cc-121">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration</span></span>
- <span data-ttu-id="dc3cc-122">**Set-AzureHDInsightDefaultStorage** yapılandırma için varsayılan depolama hesabını MyBlobStorage.blob.Core.Windows.net olarak ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="dc3cc-122">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net</span></span>
- <span data-ttu-id="dc3cc-123">**Add-AzureHDInsightStorage-** yapılandırmaya MySecondBlobStorage.blob.Core.Windows.net adlı ikinci bir depolama hesabı ekleme</span><span class="sxs-lookup"><span data-stu-id="dc3cc-123">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration</span></span>
- <span data-ttu-id="dc3cc-124">**Add-AzureHDInsightStorage** , Oozie ve bir kovan için bir</span><span class="sxs-lookup"><span data-stu-id="dc3cc-124">**Add-AzureHDInsightStorage** to add a metastore for Oozie and a metastore for Hive to the configuration</span></span>
- <span data-ttu-id="dc3cc-125">**Yeni-AzureHDInsightCluster** yeni yapılandırmayla bir HDInsight kümesi oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="dc3cc-125">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration</span></span>

## <span data-ttu-id="dc3cc-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc3cc-126">PARAMETERS</span></span>

### <span data-ttu-id="dc3cc-127">-Config</span><span class="sxs-lookup"><span data-stu-id="dc3cc-127">-Config</span></span>
<span data-ttu-id="dc3cc-128">Yapılandırma nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-128">Specifies a configuration object.</span></span>
<span data-ttu-id="dc3cc-129">Bu cmdlet, bu parametrenin belirttiği nesneye depolama hesabı bilgilerini ekler.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-129">This cmdlet adds storage account information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc3cc-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="dc3cc-130">-Profile</span></span>
<span data-ttu-id="dc3cc-131">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dc3cc-132">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc3cc-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="dc3cc-133">-StorageAccountKey</span></span>
<span data-ttu-id="dc3cc-134">Depolama hesabına erişmek için kullanılan depolama hesabı anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-134">Specifies the storage account key that is used to access a storage account.</span></span>

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

### <span data-ttu-id="dc3cc-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dc3cc-135">-StorageAccountName</span></span>
<span data-ttu-id="dc3cc-136">Eklenecek Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-136">Specifies the name of the Azure storage account to add.</span></span>

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

### <span data-ttu-id="dc3cc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3cc-137">CommonParameters</span></span>
<span data-ttu-id="dc3cc-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc3cc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3cc-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc3cc-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3cc-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc3cc-140">INPUTS</span></span>

## <span data-ttu-id="dc3cc-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc3cc-141">OUTPUTS</span></span>

## <span data-ttu-id="dc3cc-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc3cc-142">NOTES</span></span>

## <span data-ttu-id="dc3cc-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc3cc-143">RELATED LINKS</span></span>

[<span data-ttu-id="dc3cc-144">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dc3cc-144">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="dc3cc-145">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="dc3cc-145">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="dc3cc-146">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="dc3cc-146">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


