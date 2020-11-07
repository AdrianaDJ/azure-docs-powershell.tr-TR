---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: d5841a7c612bccb760a8d755fc9a1c1364cc52a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751823"
---
# <span data-ttu-id="22e08-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="22e08-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="22e08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22e08-102">SYNOPSIS</span></span>
<span data-ttu-id="22e08-103">Bir Sqoop iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="22e08-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="22e08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22e08-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22e08-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22e08-105">DESCRIPTION</span></span>
<span data-ttu-id="22e08-106">**New-AzHDInsightSqoopJobDefinition** cmdlet 'i, bir Azure HDInsight kümesiyle kullanılmak üzere bir Sqoop iş nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="22e08-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="22e08-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22e08-107">EXAMPLES</span></span>

### <span data-ttu-id="22e08-108">Örnek 1: bir Sqoop iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="22e08-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="22e08-109">Bu komut, bir Sqoop iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="22e08-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="22e08-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22e08-110">PARAMETERS</span></span>

### <span data-ttu-id="22e08-111">-Komut</span><span class="sxs-lookup"><span data-stu-id="22e08-111">-Command</span></span>
<span data-ttu-id="22e08-112">Sqoop komutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="22e08-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="22e08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e08-113">-DefaultProfile</span></span>
<span data-ttu-id="22e08-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="22e08-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22e08-115">-Dosya</span><span class="sxs-lookup"><span data-stu-id="22e08-115">-File</span></span>
<span data-ttu-id="22e08-116">Çalıştırılacak sorguyu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="22e08-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="22e08-117">Dosya, kümeyle ilişkilendirilmiş depolama hesabında kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="22e08-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="22e08-118">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="22e08-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="22e08-119">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="22e08-119">-Files</span></span>
<span data-ttu-id="22e08-120">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="22e08-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="22e08-121">-Libya</span><span class="sxs-lookup"><span data-stu-id="22e08-121">-LibDir</span></span>
<span data-ttu-id="22e08-122">Sqoop işi için kitaplık dizinini belirtir.</span><span class="sxs-lookup"><span data-stu-id="22e08-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="22e08-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="22e08-123">-StatusFolder</span></span>
<span data-ttu-id="22e08-124">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="22e08-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="22e08-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e08-125">CommonParameters</span></span>
<span data-ttu-id="22e08-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22e08-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e08-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22e08-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e08-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22e08-128">INPUTS</span></span>

### <span data-ttu-id="22e08-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="22e08-129">None</span></span>

## <span data-ttu-id="22e08-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22e08-130">OUTPUTS</span></span>

### <span data-ttu-id="22e08-131">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="22e08-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="22e08-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22e08-132">NOTES</span></span>

## <span data-ttu-id="22e08-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22e08-133">RELATED LINKS</span></span>

[<span data-ttu-id="22e08-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="22e08-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


