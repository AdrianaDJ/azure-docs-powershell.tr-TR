---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105923"
---
# <span data-ttu-id="6c9e9-101">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6c9e9-101">New-AzureHDInsightCluster</span></span>

## <span data-ttu-id="6c9e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9e9-103">HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-103">Creates an HDInsight cluster.</span></span>

## <span data-ttu-id="6c9e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c9e9-104">SYNTAX</span></span>

### <span data-ttu-id="6c9e9-105">Yapılandırmaya göre Cluster (belirli abonelik kimlik bilgileriyle) (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6c9e9-105">Cluster By Config (with Specific Subscription Credential) (Default)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6c9e9-106">Ada göre küme (belirli bir aboneliğin kimlik bilgileriyle)</span><span class="sxs-lookup"><span data-stu-id="6c9e9-106">Cluster By Name (with Specific Subscription Credential)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6c9e9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c9e9-107">DESCRIPTION</span></span>
<span data-ttu-id="6c9e9-108">Bu Azure PowerShell HDInsight sürümü kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="6c9e9-109">Bu cmdlet 'ler 1 Ocak 2017 tarafından kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="6c9e9-110">Lütfen Azure PowerShell HDInsight 'ın daha yeni sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="6c9e9-111">Küme oluşturmak için yeni HDInsight 'un nasıl kullanılacağı hakkında bilgi için [, bkz](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="6c9e9-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="6c9e9-112">Azure PowerShell 'i ve diğer yaklaşımları kullanarak işleri gönderme hakkında bilgi için, bkz: [HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="6c9e9-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="6c9e9-113">Azure PowerShell HDInsight hakkında başvuru bilgileri için [, bkz](https://msdn.microsoft.com/en-us/library/mt438705.aspx) https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6c9e9-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="6c9e9-114">**New-AzureHDInsightCluster** cmdlet 'i, belirtilen parametreleri veya **New-AzureHDInsightClusterConfig** cmdlet 'i kullanılarak oluşturulan bir yapılandırma nesnesini kullanarak bir Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-114">The **New-AzureHDInsightCluster** cmdlet creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

## <span data-ttu-id="6c9e9-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c9e9-115">EXAMPLES</span></span>

### <span data-ttu-id="6c9e9-116">Örnek 1: HDInsight kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6c9e9-116">Example 1: Create an HDInsight cluster</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="6c9e9-117">Bu örnek geçerli abonelik için bir HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-117">This example creates an HDInsight cluster for the current subscription.</span></span>

<span data-ttu-id="6c9e9-118">İlk komut, geçerli abonelik KIMLIĞINI almak için **Get-Azuyeniden gönderme Scription** cmdlet 'ini kullanır ve ardından $SubId değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="6c9e9-119">İkinci ve üçüncü komutlar MyBlobStorage ve MySecondBlobStorage için birincil depolama anahtarlarını almak üzere **Get-AzureStorageKey** cmdlet 'ini kullanır ve ardından anahtarları $Key 1 ve $Key 2 değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="6c9e9-120">Dördüncü, beşinci ve altıncı komutlar, geçerli aboneliğin ve Oozie ve kovan için kimlik bilgilerini almak üzere **Get-Credential** cmdlet 'ini kullanır ve sonra da kimlik bilgilerini değişkenlere depolar.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="6c9e9-121">Final komutu, aşağıdaki cmdlet 'leri kullanarak bir dizi işlemi gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="6c9e9-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="6c9e9-122">**New-AzureHDInsightClusterConfig-** HDInsight küme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="6c9e9-123">**Set-AzureHDInsightDefaultStorage** , yapılandırmanın varsayılan depolama hesabını MyBlobStorage.blob.Core.Windows.net olarak ayarlamak için.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="6c9e9-124">Yapılandırmaya MySecondBlobStorage.blob.core.windows.net adlı ikinci bir depolama hesabı eklemek için **Add-AzureHDInsightStorage** .</span><span class="sxs-lookup"><span data-stu-id="6c9e9-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="6c9e9-125">**Add-AzureHDInsightMetastore** , bir Oozie ve bir kovan için bir tam</span><span class="sxs-lookup"><span data-stu-id="6c9e9-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="6c9e9-126">Yeni **-AzureHDInsightCluster** yeni yapılandırmayla bir HDInsight kümesi oluşturmak için.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="6c9e9-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c9e9-127">PARAMETERS</span></span>

### <span data-ttu-id="6c9e9-128">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="6c9e9-128">-Certificate</span></span>
<span data-ttu-id="6c9e9-129">Azure aboneliği için yönetim sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-129">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-130">-Clustersizeınnodes</span><span class="sxs-lookup"><span data-stu-id="6c9e9-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="6c9e9-131">Küme için oluşturulacak veri düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-131">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-132">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="6c9e9-132">-ClusterType</span></span>
<span data-ttu-id="6c9e9-133">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-133">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-134">-Config</span><span class="sxs-lookup"><span data-stu-id="6c9e9-134">-Config</span></span>
<span data-ttu-id="6c9e9-135">**New-AzureHDInsightClusterConfig** cmdlet 'i kullanılarak oluşturulan bir yapılandırma nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-135">Specifies a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="6c9e9-136">-Credential</span></span>
<span data-ttu-id="6c9e9-137">Bir Hadoop kümesine Uzaktan erişimde kullanılan varsayılan hesap için HDInsight Kullanıcı kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-137">Specifies the user credentials for HDInsight to use for the default account that is used to remotely access a Hadoop cluster.</span></span>
<span data-ttu-id="6c9e9-138">Bu kimlik bilgileri, kullanıcının abonelik kimlik bilgilerinden farklıdır.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-138">These credentials are distinct from the subscription credentials of the user.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-139">-Datanodev,</span><span class="sxs-lookup"><span data-stu-id="6c9e9-139">-DataNodeVMSize</span></span>
<span data-ttu-id="6c9e9-140">Veri düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-140">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6c9e9-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="6c9e9-142">HDInsight kümesinin kullandığı varsayılan depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-142">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6c9e9-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="6c9e9-144">HDInsight kümesinin kullandığı varsayılan depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-144">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-145">-DefaultStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="6c9e9-145">-DefaultStorageContainerName</span></span>
<span data-ttu-id="6c9e9-146">Varsayılan Azure depolama hesabında HDInsight kümesinin kullandığı varsayılan kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-146">Specifies the name of the default container in the default Azure storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-147">Uç nokta</span><span class="sxs-lookup"><span data-stu-id="6c9e9-147">-EndPoint</span></span>
<span data-ttu-id="6c9e9-148">Azure 'a bağlanmak için kullanılacak uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-148">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="6c9e9-149">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan uç noktayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-149">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-150">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="6c9e9-150">-HeadNodeVMSize</span></span>
<span data-ttu-id="6c9e9-151">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-151">Specifies the size of the virtual machine for the head node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-152">-HostedService</span><span class="sxs-lookup"><span data-stu-id="6c9e9-152">-HostedService</span></span>
<span data-ttu-id="6c9e9-153">HDInsight hizmetinin ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-153">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="6c9e9-154">Bu parametreyi belirtmezseniz, bu cmdlet varsayılan ad boşluğunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-154">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-155">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="6c9e9-155">-IgnoreSslErrors</span></span>
<span data-ttu-id="6c9e9-156">Güvenli Yuva Katmanı (SSL) hatalarının yoksayılıp sayılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-156">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-157">-Konum</span><span class="sxs-lookup"><span data-stu-id="6c9e9-157">-Location</span></span>
<span data-ttu-id="6c9e9-158">HDInsight kümesi oluşturacağınız bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-158">Specifies the region in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-159">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c9e9-159">-Name</span></span>
<span data-ttu-id="6c9e9-160">Oluşturulacak Azure HDInsight kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-160">Specifies the name of the Azure HDInsight cluster to create.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-161">-OSType</span><span class="sxs-lookup"><span data-stu-id="6c9e9-161">-OSType</span></span>
<span data-ttu-id="6c9e9-162">Kümenin işletim sistemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-162">Specifies the operating system for a cluster.</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-163">-Profil</span><span class="sxs-lookup"><span data-stu-id="6c9e9-163">-Profile</span></span>
<span data-ttu-id="6c9e9-164">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-164">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c9e9-165">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-165">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c9e9-166">-Rdpaccessexpme</span><span class="sxs-lookup"><span data-stu-id="6c9e9-166">-RdpAccessExpiry</span></span>
<span data-ttu-id="6c9e9-167">Uzak Masaüstü Protokolü (RDP) için bir kümeye erişim için **Tarih saat** sonu</span><span class="sxs-lookup"><span data-stu-id="6c9e9-167">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-168">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="6c9e9-168">-RdpCredential</span></span>
<span data-ttu-id="6c9e9-169">Bir kümeye RDP erişimi için kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-169">Specifies the credentials for RDP access to a cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-170">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="6c9e9-170">-SshCredential</span></span>
<span data-ttu-id="6c9e9-171">HDInsight kümesinin güvenli kabuk (SSH) Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-171">Specifies the Secure Shell (SSH) user name and password for the HDInsight cluster.</span></span>
<span data-ttu-id="6c9e9-172">Bu parametre yalnızca Linux kümeler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-172">This parameter is valid only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-173">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="6c9e9-173">-SshPublicKey</span></span>
<span data-ttu-id="6c9e9-174">Bir HDInsight kümesi için SSH ortak anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-174">Specifies the SSH public key for an HDInsight cluster.</span></span>
<span data-ttu-id="6c9e9-175">Bu parametre yalnızca Linux kümeler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-175">This parameter is valid only for Linux clusters.</span></span>

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

### <span data-ttu-id="6c9e9-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6c9e9-176">-SubnetName</span></span>
<span data-ttu-id="6c9e9-177">Alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-177">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-178">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="6c9e9-178">-Subscription</span></span>
<span data-ttu-id="6c9e9-179">HDInsight kümesi oluşturacağınız Azure aboneliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-179">Specifies the Azure subscription in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-180">-Version</span><span class="sxs-lookup"><span data-stu-id="6c9e9-180">-Version</span></span>
<span data-ttu-id="6c9e9-181">Oluşturulacak HDInsight küme sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-181">Specifies the HDInsight cluster version to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-182">-Virtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="6c9e9-182">-VirtualNetworkId</span></span>
<span data-ttu-id="6c9e9-183">Kümenin sağlandıkları sanal ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-183">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-184">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="6c9e9-184">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="6c9e9-185">ZooKeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-185">Specifies the size of the virtual machine for the ZooKeeper node.</span></span>
<span data-ttu-id="6c9e9-186">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-186">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e9-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9e9-187">CommonParameters</span></span>
<span data-ttu-id="6c9e9-188">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c9e9-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9e9-189">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c9e9-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9e9-190">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c9e9-190">INPUTS</span></span>

## <span data-ttu-id="6c9e9-191">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c9e9-191">OUTPUTS</span></span>

## <span data-ttu-id="6c9e9-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c9e9-192">NOTES</span></span>

## <span data-ttu-id="6c9e9-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c9e9-193">RELATED LINKS</span></span>

[<span data-ttu-id="6c9e9-194">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="6c9e9-194">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="6c9e9-195">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="6c9e9-195">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="6c9e9-196">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6c9e9-196">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="6c9e9-197">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="6c9e9-197">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="6c9e9-198">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6c9e9-198">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="6c9e9-199">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="6c9e9-199">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)

[<span data-ttu-id="6c9e9-200">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6c9e9-200">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


