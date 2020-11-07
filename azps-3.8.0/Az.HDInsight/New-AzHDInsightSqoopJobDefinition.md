---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 2cc5acb2017a9db2bf5ed1f80ccfd1069bc1a465
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938481"
---
# <span data-ttu-id="50e6d-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="50e6d-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="50e6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="50e6d-103">Bir Sqoop iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50e6d-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="50e6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50e6d-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50e6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="50e6d-105">DESCRIPTION</span></span>
<span data-ttu-id="50e6d-106">**New-AzHDInsightSqoopJobDefinition** cmdlet 'i, bir Azure HDInsight kümesiyle kullanılmak üzere bir Sqoop iş nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="50e6d-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="50e6d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50e6d-107">EXAMPLES</span></span>

### <span data-ttu-id="50e6d-108">Örnek 1: bir Sqoop iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="50e6d-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="50e6d-109">Bu komut, bir Sqoop iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50e6d-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="50e6d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50e6d-110">PARAMETERS</span></span>

### <span data-ttu-id="50e6d-111">-Komut</span><span class="sxs-lookup"><span data-stu-id="50e6d-111">-Command</span></span>
<span data-ttu-id="50e6d-112">Sqoop komutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="50e6d-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="50e6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e6d-113">-DefaultProfile</span></span>
<span data-ttu-id="50e6d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="50e6d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50e6d-115">-Dosya</span><span class="sxs-lookup"><span data-stu-id="50e6d-115">-File</span></span>
<span data-ttu-id="50e6d-116">Çalıştırılacak sorguyu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="50e6d-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="50e6d-117">Dosya, kümeyle ilişkilendirilmiş depolama hesabında kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="50e6d-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="50e6d-118">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="50e6d-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="50e6d-119">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="50e6d-119">-Files</span></span>
<span data-ttu-id="50e6d-120">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="50e6d-120">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50e6d-121">-Libya</span><span class="sxs-lookup"><span data-stu-id="50e6d-121">-LibDir</span></span>
<span data-ttu-id="50e6d-122">Sqoop işi için kitaplık dizinini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50e6d-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="50e6d-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="50e6d-123">-StatusFolder</span></span>
<span data-ttu-id="50e6d-124">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="50e6d-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="50e6d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e6d-125">CommonParameters</span></span>
<span data-ttu-id="50e6d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50e6d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e6d-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50e6d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e6d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50e6d-128">INPUTS</span></span>

### <span data-ttu-id="50e6d-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="50e6d-129">None</span></span>

## <span data-ttu-id="50e6d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50e6d-130">OUTPUTS</span></span>

### <span data-ttu-id="50e6d-131">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="50e6d-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="50e6d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50e6d-132">NOTES</span></span>

## <span data-ttu-id="50e6d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50e6d-133">RELATED LINKS</span></span>

[<span data-ttu-id="50e6d-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="50e6d-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


