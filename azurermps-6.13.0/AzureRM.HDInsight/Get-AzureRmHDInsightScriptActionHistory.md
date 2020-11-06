---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: cadedd6441d45065344d2bf1998552b693a01301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590268"
---
# <span data-ttu-id="3f33d-101">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="3f33d-101">Get-AzureRmHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="3f33d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f33d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f33d-103">Kümenin komut dosyası eylem geçmişini alır ve ters kronolojik sırayla listeler veya önceden çalıştırılmış bir betik eyleminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="3f33d-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f33d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f33d-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f33d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f33d-105">DESCRIPTION</span></span>
<span data-ttu-id="3f33d-106">**Get-AzureRmHDInsightScriptActionHistory** cmdlet 'ı bir Azure HDInsight kümesi için komut dosyası eylem geçmişini alır ve ters kronolojik sırayla listeler veya önceden çalıştırılmış bir betik eyleminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="3f33d-106">The **Get-AzureRmHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="3f33d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f33d-107">EXAMPLES</span></span>

### <span data-ttu-id="3f33d-108">Örnek 1: kümenin komut dosyası eylemleri listesini alma</span><span class="sxs-lookup"><span data-stu-id="3f33d-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="3f33d-109">Bu komut,-Hadoop-001 kümesindeki komut dosyası eylemlerinin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="3f33d-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="3f33d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f33d-110">PARAMETERS</span></span>

### <span data-ttu-id="3f33d-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3f33d-111">-ClusterName</span></span>
<span data-ttu-id="3f33d-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f33d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3f33d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f33d-113">-DefaultProfile</span></span>
<span data-ttu-id="3f33d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3f33d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f33d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f33d-115">-ResourceGroupName</span></span>
<span data-ttu-id="3f33d-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f33d-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3f33d-117">-Scriptexecutionıd</span><span class="sxs-lookup"><span data-stu-id="3f33d-117">-ScriptExecutionId</span></span>
<span data-ttu-id="3f33d-118">Yürütülen betik eyleminin yürütme KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f33d-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f33d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f33d-119">CommonParameters</span></span>
<span data-ttu-id="3f33d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f33d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f33d-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f33d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f33d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f33d-122">INPUTS</span></span>

### <span data-ttu-id="3f33d-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3f33d-123">None</span></span>

## <span data-ttu-id="3f33d-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f33d-124">OUTPUTS</span></span>

### <span data-ttu-id="3f33d-125">Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="3f33d-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="3f33d-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f33d-126">NOTES</span></span>

## <span data-ttu-id="3f33d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f33d-127">RELATED LINKS</span></span>
