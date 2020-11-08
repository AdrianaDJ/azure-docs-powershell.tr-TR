---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF8AA7DE-1E0F-4F5B-95F6-7820AAF789F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: c36931af0b6927ef4fee26b9f8ade7db77d17db2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105920"
---
# <span data-ttu-id="5e4b1-101">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="5e4b1-101">New-AzureHDInsightClusterConfig</span></span>

## <span data-ttu-id="5e4b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e4b1-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4b1-103">Kalıcı olmayan HDInsight küme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-103">Creates a non-persisted HDInsight cluster configuration.</span></span>

## <span data-ttu-id="5e4b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e4b1-104">SYNTAX</span></span>

```
New-AzureHDInsightClusterConfig -ClusterSizeInNodes <Int32> [-HeadNodeVMSize <String>]
 [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>] [-DataNodeVMSize <String>]
 [-ZookeeperNodeVMSize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5e4b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e4b1-105">DESCRIPTION</span></span>
<span data-ttu-id="5e4b1-106">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="5e4b1-107">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="5e4b1-108">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="5e4b1-109">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="5e4b1-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="5e4b1-110">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="5e4b1-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="5e4b1-111">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e4b1-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="5e4b1-112">**New-AzureHDInsightClusterConfig** cmdlet 'i kalıcı olmayan bir Azure HDInsight küme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-112">The **New-AzureHDInsightClusterConfig** cmdlet creates a non-persisted Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="5e4b1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e4b1-113">EXAMPLES</span></span>

### <span data-ttu-id="5e4b1-114">Örnek 1: küme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="5e4b1-114">Example 1: Create a cluster configuration</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyBlobStorage.blob.core.windows.net -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="5e4b1-115">İlk komut, geçerli abonelik KIMLIĞINI almak için **Get-Azuyeniden gönderme Scription** cmdlet 'ini kullanır ve ardından $SubId değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="5e4b1-116">İkinci ve üçüncü komutlar MyBlobStorage ve MySecondBlobStorage için birincil depolama anahtarlarını almak üzere **Get-AzureStorageKey** cmdlet 'ini kullanır ve ardından anahtarları $Key 1 ve $Key 2 değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="5e4b1-117">Dördüncü, beşinci ve altıncı komutlar, geçerli aboneliğin ve Oozie ve kovan için kimlik bilgilerini almak üzere **Get-Credential** cmdlet 'ini kullanır ve sonra da kimlik bilgilerini değişkenlere depolar.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="5e4b1-118">Final komutu, aşağıdaki cmdlet 'leri kullanarak bir dizi işlemi gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="5e4b1-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="5e4b1-119">**New-AzureHDInsightClusterConfig-** HDInsight küme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="5e4b1-120">**Set-AzureHDInsightDefaultStorage** , yapılandırmanın varsayılan depolama hesabını MyBlobStorage.blob.Core.Windows.net olarak ayarlamak için.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="5e4b1-121">Yapılandırmaya MySecondBlobStorage.blob.core.windows.net adlı ikinci bir depolama hesabı eklemek için **Add-AzureHDInsightStorage** .</span><span class="sxs-lookup"><span data-stu-id="5e4b1-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="5e4b1-122">**Add-AzureHDInsightMetastore** , bir Oozie ve bir kovan için bir tam</span><span class="sxs-lookup"><span data-stu-id="5e4b1-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="5e4b1-123">Yeni **-AzureHDInsightCluster** yeni yapılandırmayla bir HDInsight kümesi oluşturmak için.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="5e4b1-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e4b1-124">PARAMETERS</span></span>

### <span data-ttu-id="5e4b1-125">-Clustersizeınnodes</span><span class="sxs-lookup"><span data-stu-id="5e4b1-125">-ClusterSizeInNodes</span></span>
<span data-ttu-id="5e4b1-126">Küme için oluşturulacak veri düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-126">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4b1-127">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="5e4b1-127">-ClusterType</span></span>
<span data-ttu-id="5e4b1-128">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-128">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4b1-129">-Datanodev,</span><span class="sxs-lookup"><span data-stu-id="5e4b1-129">-DataNodeVMSize</span></span>
<span data-ttu-id="5e4b1-130">Veri düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-130">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4b1-131">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="5e4b1-131">-HeadNodeVMSize</span></span>
<span data-ttu-id="5e4b1-132">Kümenin baş düğümünün sanal makine boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-132">Specifies the virtual machine size of the head node for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4b1-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="5e4b1-133">-Profile</span></span>
<span data-ttu-id="5e4b1-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e4b1-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e4b1-136">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5e4b1-136">-SubnetName</span></span>
<span data-ttu-id="5e4b1-137">Alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-137">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4b1-138">-Virtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="5e4b1-138">-VirtualNetworkId</span></span>
<span data-ttu-id="5e4b1-139">Kümenin sağlandıkları sanal ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-139">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4b1-140">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="5e4b1-140">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="5e4b1-141">Bir HBase veya fırtınası kümesi için ZooKeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-141">Specifies the size of the virtual machine for the ZooKeeper node for an HBase or Storm cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4b1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4b1-142">CommonParameters</span></span>
<span data-ttu-id="5e4b1-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e4b1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e4b1-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e4b1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4b1-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e4b1-145">INPUTS</span></span>

## <span data-ttu-id="5e4b1-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e4b1-146">OUTPUTS</span></span>

## <span data-ttu-id="5e4b1-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e4b1-147">NOTES</span></span>

## <span data-ttu-id="5e4b1-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e4b1-148">RELATED LINKS</span></span>

[<span data-ttu-id="5e4b1-149">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="5e4b1-149">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="5e4b1-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="5e4b1-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="5e4b1-151">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5e4b1-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="5e4b1-152">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="5e4b1-152">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


