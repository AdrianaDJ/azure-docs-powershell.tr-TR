---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: bff21d969a88282f3ba3c1d79d1f717c3c169265
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937861"
---
# <span data-ttu-id="5609d-101">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5609d-101">Set-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="5609d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5609d-102">SYNOPSIS</span></span>
<span data-ttu-id="5609d-103">Önceden çalıştırılmış bir betik eylemini kalıcı bir betik eylemi olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5609d-103">Sets a previously executed script action to be a persisted script action.</span></span>

## <span data-ttu-id="5609d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5609d-104">SYNTAX</span></span>

```
Set-AzHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5609d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5609d-105">DESCRIPTION</span></span>
<span data-ttu-id="5609d-106">**Set-AzHDInsightPersistedScriptAction** cmdlet 'i, önceden çalıştırılmış bir betik eylemini kalıcı bir betik eylemi olacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5609d-106">The **Set-AzHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="5609d-107">Belirtilen betik eyleminin daha önce başarılı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5609d-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="5609d-108">Azure HDInsight kümesi her ölçeklendiğinde betik eylemi çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="5609d-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="5609d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5609d-109">EXAMPLES</span></span>

### <span data-ttu-id="5609d-110">Örnek 1: daha önce başarılı olan bir betik eylemini kalıcı olacak veya küme ölçeğinde çalışacak şekilde ayarlama</span><span class="sxs-lookup"><span data-stu-id="5609d-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="5609d-111">Bu komut, önceki bir komut dosyası eylemini kalıcı bir betik eylemi olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5609d-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="5609d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5609d-112">PARAMETERS</span></span>

### <span data-ttu-id="5609d-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5609d-113">-ClusterName</span></span>
<span data-ttu-id="5609d-114">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5609d-114">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5609d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5609d-115">-DefaultProfile</span></span>
<span data-ttu-id="5609d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5609d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5609d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5609d-117">-ResourceGroupName</span></span>
<span data-ttu-id="5609d-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5609d-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5609d-119">-Scriptexecutionıd</span><span class="sxs-lookup"><span data-stu-id="5609d-119">-ScriptExecutionId</span></span>
<span data-ttu-id="5609d-120">Kalıcı olarak yükseltilecek komut dosyası eyleminin yürütme KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5609d-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="5609d-121">Bu betik eyleminin yükseltilmesi için başarılı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5609d-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="5609d-122">Get-AzHDInsightScriptActionHistory kullanarak betik eylemi yürütme KIMLIĞINI bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5609d-122">You can find the script action execution ID using Get-AzHDInsightScriptActionHistory.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5609d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5609d-123">CommonParameters</span></span>
<span data-ttu-id="5609d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5609d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5609d-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5609d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5609d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5609d-126">INPUTS</span></span>

### <span data-ttu-id="5609d-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5609d-127">None</span></span>

## <span data-ttu-id="5609d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5609d-128">OUTPUTS</span></span>

### <span data-ttu-id="5609d-129">System. void</span><span class="sxs-lookup"><span data-stu-id="5609d-129">System.Void</span></span>

## <span data-ttu-id="5609d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5609d-130">NOTES</span></span>

## <span data-ttu-id="5609d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5609d-131">RELATED LINKS</span></span>

[<span data-ttu-id="5609d-132">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5609d-132">Get-AzHDInsightPersistedScriptAction</span></span>](./Get-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="5609d-133">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="5609d-133">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

