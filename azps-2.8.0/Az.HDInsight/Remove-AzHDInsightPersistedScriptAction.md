---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: cfa99107875940854b9ad9c74061ec717a16c51e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751819"
---
# <span data-ttu-id="d547e-101">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d547e-101">Remove-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="d547e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d547e-102">SYNOPSIS</span></span>
<span data-ttu-id="d547e-103">Bir HDInsight kümesinden kalıcı betik eylemini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d547e-103">Removes an persisted script action from an HDInsight cluster.</span></span>

## <span data-ttu-id="d547e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d547e-104">SYNTAX</span></span>

```
Remove-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d547e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d547e-105">DESCRIPTION</span></span>
<span data-ttu-id="d547e-106">**Remove-AzHDInsightPersistedScriptAction** cmdlet 'i, belirtilen Azure HDInsight kümesinin kalıcı betik eylemleri listesinden kalıcı bir betik eylemini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d547e-106">The **Remove-AzHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="d547e-107">Kaldırılan betik, küme ölçeklendiğinde artık yürütülmez.</span><span class="sxs-lookup"><span data-stu-id="d547e-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="d547e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d547e-108">EXAMPLES</span></span>

### <span data-ttu-id="d547e-109">Örnek 1: bir kümedeki kalıcı betik eylemleri listesinden bir betik eylemini kaldırma</span><span class="sxs-lookup"><span data-stu-id="d547e-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="d547e-110">Bu komut ScriptAction adlı betik eylemini belirtilen kümedeki kalıcı betik eylemleri listesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d547e-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="d547e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d547e-111">PARAMETERS</span></span>

### <span data-ttu-id="d547e-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d547e-112">-ClusterName</span></span>
<span data-ttu-id="d547e-113">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d547e-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d547e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d547e-114">-DefaultProfile</span></span>
<span data-ttu-id="d547e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d547e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d547e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d547e-116">-Name</span></span>
<span data-ttu-id="d547e-117">Kaldırılacak olan kalıcı betik eyleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d547e-117">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="d547e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d547e-118">-ResourceGroupName</span></span>
<span data-ttu-id="d547e-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d547e-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d547e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d547e-120">CommonParameters</span></span>
<span data-ttu-id="d547e-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d547e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d547e-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d547e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d547e-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d547e-123">INPUTS</span></span>

### <span data-ttu-id="d547e-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d547e-124">None</span></span>

## <span data-ttu-id="d547e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d547e-125">OUTPUTS</span></span>

### <span data-ttu-id="d547e-126">System. void</span><span class="sxs-lookup"><span data-stu-id="d547e-126">System.Void</span></span>

## <span data-ttu-id="d547e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d547e-127">NOTES</span></span>

## <span data-ttu-id="d547e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d547e-128">RELATED LINKS</span></span>

[<span data-ttu-id="d547e-129">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d547e-129">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="d547e-130">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="d547e-130">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


