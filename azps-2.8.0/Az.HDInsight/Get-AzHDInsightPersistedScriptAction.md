---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: a437c27aaa5caea7ae0efb7ab477fe643a5c80a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751843"
---
# <span data-ttu-id="5ccf3-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5ccf3-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="5ccf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ccf3-102">SYNOPSIS</span></span>
<span data-ttu-id="5ccf3-103">Kümenin kalıcı komut dosyası eylemlerini alır ve bunları kronolojik sırada listeler veya belirli bir kalıcı betik eyleminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="5ccf3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ccf3-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ccf3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ccf3-105">DESCRIPTION</span></span>
<span data-ttu-id="5ccf3-106">**Get-AzHDInsightPersistedScriptAction** cmdlet 'ı bir Azure HDInsight kümesi için kalıcı betik eylemlerini alır ve bunları kronolojik sırada listeler veya belirli bir kalıcı betik eyleminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="5ccf3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ccf3-107">EXAMPLES</span></span>

### <span data-ttu-id="5ccf3-108">Örnek 1: kümede kalıcı betik eylemlerini alma</span><span class="sxs-lookup"><span data-stu-id="5ccf3-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="5ccf3-109">Bu komut,-Hadoop-001 adlı kümedeki kalıcı betik eylemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="5ccf3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ccf3-110">PARAMETERS</span></span>

### <span data-ttu-id="5ccf3-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5ccf3-111">-ClusterName</span></span>
<span data-ttu-id="5ccf3-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5ccf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ccf3-113">-DefaultProfile</span></span>
<span data-ttu-id="5ccf3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5ccf3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ccf3-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ccf3-115">-Name</span></span>
<span data-ttu-id="5ccf3-116">Kalıcı betik eyleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccf3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ccf3-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ccf3-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5ccf3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ccf3-119">CommonParameters</span></span>
<span data-ttu-id="5ccf3-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ccf3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ccf3-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ccf3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ccf3-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ccf3-122">INPUTS</span></span>

### <span data-ttu-id="5ccf3-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5ccf3-123">None</span></span>

## <span data-ttu-id="5ccf3-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ccf3-124">OUTPUTS</span></span>

### <span data-ttu-id="5ccf3-125">Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="5ccf3-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="5ccf3-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ccf3-126">NOTES</span></span>

## <span data-ttu-id="5ccf3-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ccf3-127">RELATED LINKS</span></span>

[<span data-ttu-id="5ccf3-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5ccf3-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="5ccf3-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5ccf3-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


