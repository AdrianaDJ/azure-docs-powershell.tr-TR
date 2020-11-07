---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 769406d0eb47672fcaaea8acfb3b3fdccd6810d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764561"
---
# <span data-ttu-id="0e10b-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0e10b-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="0e10b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e10b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e10b-103">Bir Sqoop iş nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0e10b-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e10b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e10b-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e10b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e10b-105">DESCRIPTION</span></span>
<span data-ttu-id="0e10b-106">**New-AzureRmHDInsightSqoopJobDefinition** cmdlet 'i, bir Azure HDInsight kümesiyle kullanılmak üzere bir Sqoop iş nesnesi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0e10b-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0e10b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e10b-107">EXAMPLES</span></span>

### <span data-ttu-id="0e10b-108">Örnek 1: bir Sqoop iş tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0e10b-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="0e10b-109">Bu komut, bir Sqoop iş tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0e10b-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="0e10b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e10b-110">PARAMETERS</span></span>

### <span data-ttu-id="0e10b-111">-Komut</span><span class="sxs-lookup"><span data-stu-id="0e10b-111">-Command</span></span>
<span data-ttu-id="0e10b-112">Sqoop komutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e10b-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="0e10b-113">-Dosya</span><span class="sxs-lookup"><span data-stu-id="0e10b-113">-File</span></span>
<span data-ttu-id="0e10b-114">Çalıştırılacak sorguyu içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e10b-114">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="0e10b-115">Dosya, kümeyle ilişkilendirilmiş depolama hesabında kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0e10b-115">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="0e10b-116">*Sorgu* parametresi yerine bu parametreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e10b-116">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="0e10b-117">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="0e10b-117">-Files</span></span>
<span data-ttu-id="0e10b-118">Bir kovan işiyle ilişkili dosyalar koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e10b-118">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="0e10b-119">-Libya</span><span class="sxs-lookup"><span data-stu-id="0e10b-119">-LibDir</span></span>
<span data-ttu-id="0e10b-120">Sqoop işi için kitaplık dizinini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e10b-120">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="0e10b-121">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="0e10b-121">-StatusFolder</span></span>
<span data-ttu-id="0e10b-122">İş için standart çıktıları ve hata çıktılarını içeren klasörün konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e10b-122">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="0e10b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e10b-123">-DefaultProfile</span></span>
<span data-ttu-id="0e10b-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e10b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e10b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e10b-125">CommonParameters</span></span>
<span data-ttu-id="0e10b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e10b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e10b-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e10b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e10b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e10b-128">INPUTS</span></span>

## <span data-ttu-id="0e10b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e10b-129">OUTPUTS</span></span>

### <span data-ttu-id="0e10b-130">Microsoft. Azure. Commands. HDInsight. modeller. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0e10b-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="0e10b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e10b-131">NOTES</span></span>

## <span data-ttu-id="0e10b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e10b-132">RELATED LINKS</span></span>

[<span data-ttu-id="0e10b-133">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0e10b-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


