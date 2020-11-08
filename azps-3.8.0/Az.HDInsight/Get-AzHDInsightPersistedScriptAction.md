---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 56056e2933254401645a30e190a3a181b0c4514f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938507"
---
# <span data-ttu-id="ba6c1-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ba6c1-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="ba6c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba6c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6c1-103">Kümenin kalıcı komut dosyası eylemlerini alır ve bunları kronolojik sırada listeler veya belirli bir kalıcı betik eyleminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ba6c1-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="ba6c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba6c1-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba6c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba6c1-105">DESCRIPTION</span></span>
<span data-ttu-id="ba6c1-106">**Get-AzHDInsightPersistedScriptAction** cmdlet 'ı bir Azure HDInsight kümesi için kalıcı betik eylemlerini alır ve bunları kronolojik sırada listeler veya belirli bir kalıcı betik eyleminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ba6c1-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="ba6c1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba6c1-107">EXAMPLES</span></span>

### <span data-ttu-id="ba6c1-108">Örnek 1: kümede kalıcı betik eylemlerini alma</span><span class="sxs-lookup"><span data-stu-id="ba6c1-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="ba6c1-109">Bu komut,-Hadoop-001 adlı kümedeki kalıcı betik eylemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="ba6c1-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="ba6c1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba6c1-110">PARAMETERS</span></span>

### <span data-ttu-id="ba6c1-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ba6c1-111">-ClusterName</span></span>
<span data-ttu-id="ba6c1-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba6c1-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ba6c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6c1-113">-DefaultProfile</span></span>
<span data-ttu-id="ba6c1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ba6c1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba6c1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba6c1-115">-Name</span></span>
<span data-ttu-id="ba6c1-116">Kalıcı betik eyleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba6c1-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="ba6c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba6c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba6c1-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba6c1-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ba6c1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6c1-119">CommonParameters</span></span>
<span data-ttu-id="ba6c1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba6c1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6c1-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba6c1-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6c1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba6c1-122">INPUTS</span></span>

### <span data-ttu-id="ba6c1-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ba6c1-123">None</span></span>

## <span data-ttu-id="ba6c1-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba6c1-124">OUTPUTS</span></span>

### <span data-ttu-id="ba6c1-125">Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="ba6c1-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="ba6c1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba6c1-126">NOTES</span></span>

## <span data-ttu-id="ba6c1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba6c1-127">RELATED LINKS</span></span>

[<span data-ttu-id="ba6c1-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ba6c1-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="ba6c1-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="ba6c1-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)

