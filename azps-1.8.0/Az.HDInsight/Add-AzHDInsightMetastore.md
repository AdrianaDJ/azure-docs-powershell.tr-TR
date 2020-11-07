---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: f43e484d4e4ced7aadcc1fc7916cefb6e34784df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916671"
---
# <span data-ttu-id="73ec2-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="73ec2-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="73ec2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="73ec2-103">Bir SQL veritabanını yığın veya Oozie metaser olarak bir küme yapılandırma nesnesine ekler.</span><span class="sxs-lookup"><span data-stu-id="73ec2-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="73ec2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73ec2-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73ec2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="73ec2-105">DESCRIPTION</span></span>
<span data-ttu-id="73ec2-106">**Add-AzHDInsightMetastore** cmdlet 'i, New-AzHDInsightClusterConfig cmdlet 'i tarafından oluşturulan HDInsight yapılandırma nesnesine bir Hive veya Oozie metaser ekler.</span><span class="sxs-lookup"><span data-stu-id="73ec2-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="73ec2-107">Metaser, kovanı, Oozie veya her ikisi için meta verileri depolamak için kullanılan bir SQL veritabanıdır.</span><span class="sxs-lookup"><span data-stu-id="73ec2-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="73ec2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73ec2-108">EXAMPLES</span></span>

### <span data-ttu-id="73ec2-109">Örnek 1: küme yapılandırma nesnesine SQL veritabanı eklemesi ekleme</span><span class="sxs-lookup"><span data-stu-id="73ec2-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="73ec2-110">Bu komut,-Hadoop-001 adlı kümeye SQL veritabanı eklemesi ekler.</span><span class="sxs-lookup"><span data-stu-id="73ec2-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="73ec2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73ec2-111">PARAMETERS</span></span>

### <span data-ttu-id="73ec2-112">-Config</span><span class="sxs-lookup"><span data-stu-id="73ec2-112">-Config</span></span>
<span data-ttu-id="73ec2-113">Bu cmdlet 'in değiştirdiği HDInsight küme yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="73ec2-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="73ec2-114">Bu nesne, **New-AzHDInsightClusterConfig** cmdlet 'i tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="73ec2-114">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73ec2-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="73ec2-115">-Credential</span></span>
<span data-ttu-id="73ec2-116">AzureSQL Server veritabanı için kullanılacak kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="73ec2-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

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

### <span data-ttu-id="73ec2-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="73ec2-117">-DatabaseName</span></span>
<span data-ttu-id="73ec2-118">Bu meta veri için kullanılacak AzureSQL Server örneğindeki veritabanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="73ec2-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ec2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ec2-119">-DefaultProfile</span></span>
<span data-ttu-id="73ec2-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="73ec2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73ec2-121">-Metastoyeniden yazma</span><span class="sxs-lookup"><span data-stu-id="73ec2-121">-MetastoreType</span></span>
<span data-ttu-id="73ec2-122">Metassıneraç türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="73ec2-122">Specifies the type of metastore.</span></span>
<span data-ttu-id="73ec2-123">Olası değerler Hivemetasınor Oozıemetas,.</span><span class="sxs-lookup"><span data-stu-id="73ec2-123">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ec2-124">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="73ec2-124">-SqlAzureServerName</span></span>
<span data-ttu-id="73ec2-125">Bu metasınfor bu meta</span><span class="sxs-lookup"><span data-stu-id="73ec2-125">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="73ec2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ec2-126">CommonParameters</span></span>
<span data-ttu-id="73ec2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73ec2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ec2-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73ec2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ec2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73ec2-129">INPUTS</span></span>

### <span data-ttu-id="73ec2-130">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="73ec2-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="73ec2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73ec2-131">OUTPUTS</span></span>

### <span data-ttu-id="73ec2-132">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="73ec2-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="73ec2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73ec2-133">NOTES</span></span>

## <span data-ttu-id="73ec2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73ec2-134">RELATED LINKS</span></span>

[<span data-ttu-id="73ec2-135">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="73ec2-135">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

