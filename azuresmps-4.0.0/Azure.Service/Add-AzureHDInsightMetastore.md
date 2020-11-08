---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105723"
---
# <span data-ttu-id="27106-101">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="27106-101">Add-AzureHDInsightMetastore</span></span>

## <span data-ttu-id="27106-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27106-102">SYNOPSIS</span></span>
<span data-ttu-id="27106-103">HDInsight küme yapılandırmasına SQL Server veritabanı hesabı ekler.</span><span class="sxs-lookup"><span data-stu-id="27106-103">Adds a SQL Server database account to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="27106-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27106-104">SYNTAX</span></span>

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="27106-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="27106-105">DESCRIPTION</span></span>
<span data-ttu-id="27106-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="27106-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="27106-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="27106-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="27106-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="27106-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="27106-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="27106-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="27106-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="27106-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="27106-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="27106-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="27106-112">**Add-AzureHDInsightMetastore** cmdlet 'ı, **Yeni-AzureHDInsightClusterConfig** cmdlet 'ı tarafından oluşturulan bir Azure HDInsight yapılandırmasına Microsoft SQL Server veritabanı ekler.</span><span class="sxs-lookup"><span data-stu-id="27106-112">The **Add-AzureHDInsightMetastore** cmdlet adds a Microsoft SQL Server database to an Azure HDInsight configuration that is created by the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>
<span data-ttu-id="27106-113">Veritabanı, kovan veya Oozie veya her ikisi için meta verileri depolamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27106-113">The database is used to store metadata for Hive or Oozie, or both.</span></span>

## <span data-ttu-id="27106-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27106-114">EXAMPLES</span></span>

### <span data-ttu-id="27106-115">Örnek 1: bir meta</span><span class="sxs-lookup"><span data-stu-id="27106-115">Example 1: Add a metastore</span></span>
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

<span data-ttu-id="27106-116">Bu komut, bir HDInsight kümesi için bir Hive örneği olarak hizmet verecek olan ContosoSQLServer adlı bir SQL Server veritabanı ekler.</span><span class="sxs-lookup"><span data-stu-id="27106-116">This command adds a SQL Server database named ContosoSQLServer to serve as a Hive metastore for an HDInsight cluster.</span></span>

### <span data-ttu-id="27106-117">Örnek 2: depolama alanını yapılandırma ve metastores ekleme</span><span class="sxs-lookup"><span data-stu-id="27106-117">Example 2: Configure storage and add metastores</span></span>
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

<span data-ttu-id="27106-118">İlk komut, geçerli abonelik KIMLIĞINI almak için **Get-Azuyeniden gönderme Scription** cmdlet 'ini kullanır ve ardından $SubId değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="27106-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="27106-119">İkinci ve üçüncü komutlar MyBlobStorage ve MySecondBlobStorage için birincil depolama anahtarlarını almak üzere **Get-AzureStorageKey** cmdlet 'ini kullanır ve ardından anahtarları $Key 1 ve $Key 2 değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="27106-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="27106-120">Dördüncü, beşinci ve altıncı komutlar, geçerli aboneliğin ve Oozie ve kovan için kimlik bilgilerini almak üzere **Get-Credential** cmdlet 'ini kullanır ve sonra da kimlik bilgilerini değişkenlere depolar.</span><span class="sxs-lookup"><span data-stu-id="27106-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="27106-121">Final komutu, aşağıdaki cmdlet 'leri kullanarak bir dizi işlemi gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="27106-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="27106-122">**New-AzureHDInsightClusterConfig-** HDInsight küme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27106-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="27106-123">**Set-AzureHDInsightDefaultStorage** , yapılandırmanın varsayılan depolama hesabını MyBlobStorage.blob.Core.Windows.net olarak ayarlamak için.</span><span class="sxs-lookup"><span data-stu-id="27106-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="27106-124">Yapılandırmaya MySecondBlobStorage.blob.core.windows.net adlı ikinci bir depolama hesabı eklemek için **Add-AzureHDInsightStorage** .</span><span class="sxs-lookup"><span data-stu-id="27106-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="27106-125">**Add-AzureHDInsightMetastore** , bir Oozie ve bir kovan için bir tam</span><span class="sxs-lookup"><span data-stu-id="27106-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="27106-126">Yeni **-AzureHDInsightCluster** yeni yapılandırmayla bir HDInsight kümesi oluşturmak için.</span><span class="sxs-lookup"><span data-stu-id="27106-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="27106-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27106-127">PARAMETERS</span></span>

### <span data-ttu-id="27106-128">-Config</span><span class="sxs-lookup"><span data-stu-id="27106-128">-Config</span></span>
<span data-ttu-id="27106-129">Yapılandırma nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27106-129">Specifies a configuration object.</span></span>
<span data-ttu-id="27106-130">Bu cmdlet, bu parametrenin belirttiği yapılandırma nesnesine bazı bilgileri ekler.</span><span class="sxs-lookup"><span data-stu-id="27106-130">This cmdlet adds metastore information to the configuration object that this parameter specifies.</span></span>

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

### <span data-ttu-id="27106-131">-Credential</span><span class="sxs-lookup"><span data-stu-id="27106-131">-Credential</span></span>
<span data-ttu-id="27106-132">SQL Server veritabanına erişmek için kullanılan kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27106-132">Specifies the credentials that are used to access a SQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27106-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="27106-133">-DatabaseName</span></span>
<span data-ttu-id="27106-134">Kovan veya Oozie meta verilerini depolayacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27106-134">Specifies the name of the database to store Hive or Oozie metadata.</span></span>

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

### <span data-ttu-id="27106-135">-Metastoyeniden yazma</span><span class="sxs-lookup"><span data-stu-id="27106-135">-MetastoreType</span></span>
<span data-ttu-id="27106-136">Metasınaç türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="27106-136">Specifies the metastore type.</span></span>
<span data-ttu-id="27106-137">Bu parametre için kabul edilebilir değerler: hivemetasınor oozıemetas</span><span class="sxs-lookup"><span data-stu-id="27106-137">The acceptable values for this parameter are: HiveMetaStore or OozieMetaStore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27106-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="27106-138">-Profile</span></span>
<span data-ttu-id="27106-139">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27106-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="27106-140">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="27106-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="27106-141">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="27106-141">-SqlAzureServerName</span></span>
<span data-ttu-id="27106-142">Meta verilerin depolanacağı veritabanını içeren SQL Server 'ın tam etki alanı adını (FQDN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="27106-142">Specifies the fully qualified domain name (FQDN) of the SQL Server that contains the database to store metadata.</span></span>

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

### <span data-ttu-id="27106-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27106-143">CommonParameters</span></span>
<span data-ttu-id="27106-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27106-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27106-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27106-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27106-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27106-146">INPUTS</span></span>

## <span data-ttu-id="27106-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27106-147">OUTPUTS</span></span>

## <span data-ttu-id="27106-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27106-148">NOTES</span></span>

## <span data-ttu-id="27106-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27106-149">RELATED LINKS</span></span>

[<span data-ttu-id="27106-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="27106-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="27106-151">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="27106-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="27106-152">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="27106-152">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="27106-153">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="27106-153">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
