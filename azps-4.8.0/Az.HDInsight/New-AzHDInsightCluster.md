---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 9008cb1dba2c39a2c552b2395f4115ca50a17fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109080"
---
# <span data-ttu-id="4c6fa-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4c6fa-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="4c6fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="4c6fa-103">Geçerli abonelik için belirtilen kaynak grubunda bir Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="4c6fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c6fa-104">SYNTAX</span></span>

### <span data-ttu-id="4c6fa-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c6fa-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>]
 [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c6fa-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4c6fa-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c6fa-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4c6fa-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c6fa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c6fa-108">DESCRIPTION</span></span>
<span data-ttu-id="4c6fa-109">New-AzHDInsightCluster belirtilen parametreleri kullanarak veya New-AzHDInsightClusterConfig cmdlet 'i kullanılarak oluşturulan bir yapılandırma nesnesi kullanarak Azure HDInsight kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="4c6fa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c6fa-110">EXAMPLES</span></span>

### <span data-ttu-id="4c6fa-111">Örnek 1: Azure HDInsight kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c6fa-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="4c6fa-112">Bu komut geçerli abonelikte bir küme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="4c6fa-113">Örnek 2: müşteri tarafından yönetilen anahtar disk şifrelemesi ile küme oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c6fa-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"
        $clusterCreds = Get-Credential

        # Customer-managed Key info
        $assignedIdentity = "your-ami-resource-id"
        $encryptionKeyName = "new-key"
        $encryptionVaultUri = "https://MyKeyVault.vault.azure.net"
        $encryptionKeyVersion = "00000000000000000000000000000000"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Spark `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="4c6fa-114">Örnek 3: aktarma sırasında şifrelemeyi sağlayan bir Azure HDInsight kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c6fa-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="4c6fa-115">Örnek 4: özel bağlantı özelliğiyle bir Azure HDInsight kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c6fa-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Virtual network info
        $virtualNetworkId="yourvnetresourceid"
        $subnetName="yoursubnetresourceid"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="4c6fa-116">Örnek 5: konakta şifrelemeyi sağlayan bir Azure HDInsight kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c6fa-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="4c6fa-117">Örnek 6: otomatik ölçeklendirme sağlayan bir Azure HDInsight kümesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create autoscale configuration
        $autoscaleConfiguration=New-AzHDInsightClusterAutoscaleConfiguration `
            -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

## <span data-ttu-id="4c6fa-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c6fa-118">PARAMETERS</span></span>

### <span data-ttu-id="4c6fa-119">-Aadtenantıd</span><span class="sxs-lookup"><span data-stu-id="4c6fa-119">-AadTenantId</span></span>
<span data-ttu-id="4c6fa-120">Azure Data Lake Store 'a erişirken kullanılacak Azure AD kiracı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-120">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-121">-Addistorageaccounts</span><span class="sxs-lookup"><span data-stu-id="4c6fa-121">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="4c6fa-122">Kümenin ek Azure depolama hesaplarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-122">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="4c6fa-123">Alternatif olarak Add-AzHDInsightStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-123">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4c6fa-124">-ApplicationId</span></span>
<span data-ttu-id="4c6fa-125">Azure Data Lake 'e erişmek için hizmet sorumlusu uygulama kimliğini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-125">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-126">-Atandıdentity</span><span class="sxs-lookup"><span data-stu-id="4c6fa-126">-AssignedIdentity</span></span>
<span data-ttu-id="4c6fa-127">Atanan kimliği alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-127">Gets or sets the assigned identity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-128">-Otomatik ölçek yapılandırması</span><span class="sxs-lookup"><span data-stu-id="4c6fa-128">-AutoscaleConfiguration</span></span>
<span data-ttu-id="4c6fa-129">Otomatik ölçeklendirme yapılandırmasını alır veya ayarlar</span><span class="sxs-lookup"><span data-stu-id="4c6fa-129">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-130">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4c6fa-130">-CertificateFileContents</span></span>
<span data-ttu-id="4c6fa-131">Azure Data Lake Store 'a erişirken kullanılacak sertifikanın dosya içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-131">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-132">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4c6fa-132">-CertificateFilePath</span></span>
<span data-ttu-id="4c6fa-133">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-133">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4c6fa-134">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-134">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4c6fa-135">-CertificatePassword</span></span>
<span data-ttu-id="4c6fa-136">Hizmet sorumlusu olarak kimlik doğrulaması için kullanılacak sertifikanın parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-136">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4c6fa-137">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-138">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4c6fa-138">-ClusterName</span></span>
<span data-ttu-id="4c6fa-139">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-139">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-140">-Clustersizeınnodes</span><span class="sxs-lookup"><span data-stu-id="4c6fa-140">-ClusterSizeInNodes</span></span>
<span data-ttu-id="4c6fa-141">Kümenin çalışan düğümü sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-141">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-142">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="4c6fa-142">-ClusterTier</span></span>
<span data-ttu-id="4c6fa-143">HDInsight küme katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-143">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="4c6fa-144">Varsayılan olarak bu standart olur.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-144">By default, this is Standard.</span></span>
<span data-ttu-id="4c6fa-145">Premium katmanı yalnızca Linux kümeleriyle kullanılabilir ve bazı yeni özelliklerin kullanılmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-145">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-146">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="4c6fa-146">-ClusterType</span></span>
<span data-ttu-id="4c6fa-147">Oluşturulacak kümenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-147">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="4c6fa-148">Seçenekler: Hadoop, HBase, fırtınası, Spark, ıNTERACTIVEKOVANı, Kafka ve RServer</span><span class="sxs-lookup"><span data-stu-id="4c6fa-148">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-149">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="4c6fa-149">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-150">-Config</span><span class="sxs-lookup"><span data-stu-id="4c6fa-150">-Config</span></span>
<span data-ttu-id="4c6fa-151">Kümeyi oluştururken kullanılacak küme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-151">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="4c6fa-152">Bu nesne New-AzHDInsightClusterConfig cmdlet kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-152">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-153">-Yapılandırmalar</span><span class="sxs-lookup"><span data-stu-id="4c6fa-153">-Configurations</span></span>
<span data-ttu-id="4c6fa-154">Bu HDInsight kümesinin yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-154">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="4c6fa-155">Alternatif olarak Add-AzHDInsightConfigValues cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-155">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c6fa-156">-DefaultProfile</span></span>
<span data-ttu-id="4c6fa-157">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4c6fa-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-158">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4c6fa-158">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="4c6fa-159">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının hesap anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-159">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4c6fa-160">Alternatif olarak Set-AzHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-160">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-161">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4c6fa-161">-DefaultStorageAccountName</span></span>
<span data-ttu-id="4c6fa-162">HDInsight kümesinin kullanacağı varsayılan Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-162">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4c6fa-163">Alternatif olarak Set-AzHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-163">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-164">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4c6fa-164">-DefaultStorageAccountType</span></span>
<span data-ttu-id="4c6fa-165">HDInsight kümesinin kullanacağı varsayılan depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-165">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="4c6fa-166">Olası değerler AzureStorage and AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-166">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="4c6fa-167">Belirtilmemişse, varsayılan olarak AzureStorage kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-167">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-168">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4c6fa-168">-DefaultStorageContainer</span></span>
<span data-ttu-id="4c6fa-169">Varsayılan Azure depolama hesabında HDInsight kümesinin kullanacağı varsayılan kapsayıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-169">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4c6fa-170">Alternatif olarak Set-AzHDInsightDefaultStorage cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-170">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-171">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="4c6fa-171">-DefaultStorageRootPath</span></span>
<span data-ttu-id="4c6fa-172">Veri Lake Store hesabında HDInsight kümesinin varsayılan FileSystem olarak kullanacağı yol önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-172">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-173">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="4c6fa-173">-DisksPerWorkerNode</span></span>
<span data-ttu-id="4c6fa-174">Kümedeki çalışan düğümü rolü için disk sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-174">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-175">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="4c6fa-175">-EdgeNodeSize</span></span>
<span data-ttu-id="4c6fa-176">Edge düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-176">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="4c6fa-177">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-177">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="4c6fa-178">Bu parametre yalnızca RServer kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-178">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-179">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="4c6fa-179">-EncryptionAlgorithm</span></span>
<span data-ttu-id="4c6fa-180">Şifreleme algoritmasını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-180">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-181">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="4c6fa-181">-EncryptionAtHost</span></span>
<span data-ttu-id="4c6fa-182">Ana bilgisayarda şifrelemeyi etkinleştirip etkinleştirmeyeceğinizi belirten bayrağı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-182">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-183">-Şifrelememe</span><span class="sxs-lookup"><span data-stu-id="4c6fa-183">-EncryptionInTransit</span></span>
<span data-ttu-id="4c6fa-184">İletimde şifrelemeyi etkinleştir 'in etkin olup olmadığını belirten bayrağı alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-184">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-185">-Encryptionanahtaradı</span><span class="sxs-lookup"><span data-stu-id="4c6fa-185">-EncryptionKeyName</span></span>
<span data-ttu-id="4c6fa-186">Şifreleme anahtarı adını alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-186">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-187">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="4c6fa-187">-EncryptionKeyVersion</span></span>
<span data-ttu-id="4c6fa-188">Şifreleme anahtarı sürümünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-188">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-189">-Şifrelemem</span><span class="sxs-lookup"><span data-stu-id="4c6fa-189">-EncryptionVaultUri</span></span>
<span data-ttu-id="4c6fa-190">Şifreleme Kasası URI 'sini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-190">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-191">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="4c6fa-191">-HeadNodeSize</span></span>
<span data-ttu-id="4c6fa-192">Head düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-192">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="4c6fa-193">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-193">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-194">-Hivemetas,</span><span class="sxs-lookup"><span data-stu-id="4c6fa-194">-HiveMetastore</span></span>
<span data-ttu-id="4c6fa-195">Kovan meta verilerinin depolanacağı SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-195">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="4c6fa-196">Alternatif olarak Add-AzHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-196">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-197">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4c6fa-197">-HttpCredential</span></span>
<span data-ttu-id="4c6fa-198">Kümenin küme oturum açma (HTTP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-198">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-199">-Konum</span><span class="sxs-lookup"><span data-stu-id="4c6fa-199">-Location</span></span>
<span data-ttu-id="4c6fa-200">Kümenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-200">Specifies the location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-201">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="4c6fa-201">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="4c6fa-202">Desteklenen en düşük TLS sürümünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-202">Gets or sets the minimal supported TLS version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-203">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="4c6fa-203">-ObjectId</span></span>
<span data-ttu-id="4c6fa-204">Kümeyi temsil eden Azure AD hizmeti sorumlusunun Azure AD nesnesi KIMLIĞINI (GUID) belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-204">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="4c6fa-205">Küme, Azure Data Lake Store 'a erişirken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-205">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-206">-Oozıemetas</span><span class="sxs-lookup"><span data-stu-id="4c6fa-206">-OozieMetastore</span></span>
<span data-ttu-id="4c6fa-207">Oozie meta verilerini depolayacak SQL veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-207">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="4c6fa-208">Alternatif olarak Add-AzHDInsightMetastore cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-208">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-209">-OSType</span><span class="sxs-lookup"><span data-stu-id="4c6fa-209">-OSType</span></span>
<span data-ttu-id="4c6fa-210">Kümenin işletim sistemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-210">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="4c6fa-211">Seçenekler şunlardır: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="4c6fa-211">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-212">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="4c6fa-212">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="4c6fa-213">Giden erişim türünü genel ağa alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-213">Gets or sets the outbound access type to the public network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-214">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="4c6fa-214">-PublicNetworkAccessType</span></span>
<span data-ttu-id="4c6fa-215">Genel ağ erişim türünü alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-215">Gets or sets the public network access type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-216">-Rdpaccessexpme</span><span class="sxs-lookup"><span data-stu-id="4c6fa-216">-RdpAccessExpiry</span></span>
<span data-ttu-id="4c6fa-217">Uzak Masaüstü Protokolü (RDP) için bir kümeye erişim için tarih saat sonu</span><span class="sxs-lookup"><span data-stu-id="4c6fa-217">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-218">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="4c6fa-218">-RdpCredential</span></span>
<span data-ttu-id="4c6fa-219">Kümenin uzak masaüstü (RDP) kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-219">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="4c6fa-220">Bu yalnızca Windows kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-220">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-221">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c6fa-221">-ResourceGroupName</span></span>
<span data-ttu-id="4c6fa-222">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-222">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-223">-Betikler</span><span class="sxs-lookup"><span data-stu-id="4c6fa-223">-ScriptActions</span></span>
<span data-ttu-id="4c6fa-224">Küme oluşturma sonunda kümede çalışacak komut dosyası eylemlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-224">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="4c6fa-225">Alternatif olarak Add-AzHDInsightScriptAction kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-225">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-226">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="4c6fa-226">-SecurityProfile</span></span>
<span data-ttu-id="4c6fa-227">Güvenli küme oluşturmak için kullanılan güvenlikle ilgili özellikleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-227">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="4c6fa-228">Alternatif olarak Add-AzHDInsightSecurityProfile cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-228">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-229">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="4c6fa-229">-SshCredential</span></span>
<span data-ttu-id="4c6fa-230">SSH bağlantılarında kullanılacak SSH kimlik bilgisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-230">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="4c6fa-231">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-231">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-232">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4c6fa-232">-SshPublicKey</span></span>
<span data-ttu-id="4c6fa-233">SSH bağlantılarında kullanılacak ortak anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-233">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="4c6fa-234">Bu yalnızca Linux kümeleri içindir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-234">This is only for Linux clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-235">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4c6fa-235">-SubnetName</span></span>
<span data-ttu-id="4c6fa-236">Küme için seçilen sanal ağdaki bir alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-236">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-237">-Version</span><span class="sxs-lookup"><span data-stu-id="4c6fa-237">-Version</span></span>
<span data-ttu-id="4c6fa-238">HDInsight kümesinin HDI sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-238">Specifies the HDI version of the HDInsight cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-239">-Virtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="4c6fa-239">-VirtualNetworkId</span></span>
<span data-ttu-id="4c6fa-240">Kümenin sağlandıkları sanal ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-240">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-241">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="4c6fa-241">-WorkerNodeSize</span></span>
<span data-ttu-id="4c6fa-242">Çalışan düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-242">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="4c6fa-243">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-243">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-244">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="4c6fa-244">-ZookeeperNodeSize</span></span>
<span data-ttu-id="4c6fa-245">Zookeeper düğümünün sanal makinesinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-245">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="4c6fa-246">Kabul edilebilir VM boyutlarında Get-AzVMSize kullanın ve HDInsight 'ın fiyatlandırma sayfasına bakın.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-246">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="4c6fa-247">Bu parametre yalnızca HBase veya fırtınası kümeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-247">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c6fa-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c6fa-248">CommonParameters</span></span>
<span data-ttu-id="4c6fa-249">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c6fa-250">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4c6fa-250">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c6fa-251">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c6fa-251">INPUTS</span></span>

### <span data-ttu-id="4c6fa-252">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4c6fa-252">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4c6fa-253">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c6fa-253">OUTPUTS</span></span>

### <span data-ttu-id="4c6fa-254">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4c6fa-254">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="4c6fa-255">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c6fa-255">NOTES</span></span>
<span data-ttu-id="4c6fa-256">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, Hadoop, HDInsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="4c6fa-256">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="4c6fa-257">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c6fa-257">RELATED LINKS</span></span>

[<span data-ttu-id="4c6fa-258">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4c6fa-258">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

