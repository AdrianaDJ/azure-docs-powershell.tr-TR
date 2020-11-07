---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: d0ca241cc29bedcd3a34f866fa2b7a19fceb0745
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764848"
---
# <span data-ttu-id="5bca0-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5bca0-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="5bca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bca0-102">SYNOPSIS</span></span>
<span data-ttu-id="5bca0-103">Kümenin kalıcı komut dosyası eylemlerini alır ve bunları kronolojik sırada listeler veya belirli bir kalıcı betik eyleminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5bca0-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bca0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5bca0-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bca0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bca0-105">DESCRIPTION</span></span>
<span data-ttu-id="5bca0-106">**Get-AzureRmHDInsightPersistedScriptAction** cmdlet 'ı bir Azure HDInsight kümesi için kalıcı betik eylemlerini alır ve bunları kronolojik sırada listeler veya belirli bir kalıcı betik eyleminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="5bca0-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="5bca0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5bca0-107">EXAMPLES</span></span>

### <span data-ttu-id="5bca0-108">Örnek 1: kümede kalıcı betik eylemlerini alma</span><span class="sxs-lookup"><span data-stu-id="5bca0-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="5bca0-109">Bu komut,-Hadoop-001 adlı kümedeki kalıcı betik eylemlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5bca0-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="5bca0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5bca0-110">PARAMETERS</span></span>

### <span data-ttu-id="5bca0-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5bca0-111">-ClusterName</span></span>
<span data-ttu-id="5bca0-112">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bca0-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5bca0-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="5bca0-113">-Name</span></span>
<span data-ttu-id="5bca0-114">Kalıcı betik eyleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bca0-114">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="5bca0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bca0-115">-ResourceGroupName</span></span>
<span data-ttu-id="5bca0-116">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bca0-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5bca0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bca0-117">-DefaultProfile</span></span>
<span data-ttu-id="5bca0-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5bca0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bca0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bca0-119">CommonParameters</span></span>
<span data-ttu-id="5bca0-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5bca0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bca0-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bca0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bca0-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5bca0-122">INPUTS</span></span>

## <span data-ttu-id="5bca0-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5bca0-123">OUTPUTS</span></span>

### <span data-ttu-id="5bca0-124">System. Koleksiyonlar. Generic. IList ' 1 [Microsoft. Azure. Commands. HDInsight. modeller. Management. AzureHDInsightRuntimeScriptAction]</span><span class="sxs-lookup"><span data-stu-id="5bca0-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction]</span></span>

## <span data-ttu-id="5bca0-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5bca0-125">NOTES</span></span>

## <span data-ttu-id="5bca0-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5bca0-126">RELATED LINKS</span></span>

[<span data-ttu-id="5bca0-127">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5bca0-127">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="5bca0-128">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5bca0-128">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


