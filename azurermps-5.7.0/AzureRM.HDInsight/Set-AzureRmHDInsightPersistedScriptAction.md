---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92F21752-4FB6-4162-B542-DA25ACA3340B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 28b95833e9221e5ecaa05ab33a6e2518c7cca1a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764717"
---
# <span data-ttu-id="dfd58-101">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="dfd58-101">Set-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="dfd58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfd58-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd58-103">Önceden çalıştırılmış bir betik eylemini kalıcı bir betik eylemi olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dfd58-103">Sets a previously executed script action to be a persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfd58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dfd58-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-ScriptExecutionId] <Int64>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfd58-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dfd58-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd58-106">**Set-AzureRmHDInsightPersistedScriptAction** cmdlet 'i, önceden çalıştırılmış bir betik eylemini kalıcı bir betik eylemi olacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dfd58-106">The **Set-AzureRmHDInsightPersistedScriptAction** cmdlet sets a previously executed script action to be a persisted script action.</span></span>
<span data-ttu-id="dfd58-107">Belirtilen betik eyleminin daha önce başarılı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfd58-107">The specified script action must have previously succeeded.</span></span>
<span data-ttu-id="dfd58-108">Azure HDInsight kümesi her ölçeklendiğinde betik eylemi çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="dfd58-108">The script action will run each time the Azure HDInsight cluster is scaled up.</span></span>

## <span data-ttu-id="dfd58-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dfd58-109">EXAMPLES</span></span>

### <span data-ttu-id="dfd58-110">Örnek 1: daha önce başarılı olan bir betik eylemini kalıcı olacak veya küme ölçeğinde çalışacak şekilde ayarlama</span><span class="sxs-lookup"><span data-stu-id="dfd58-110">Example 1: Set a previously successful script action to be persisted, or run on cluster scale up</span></span>
```
PS C:\>Set-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -ScriptExecutionId "<id>"
```

<span data-ttu-id="dfd58-111">Bu komut, önceki bir komut dosyası eylemini kalıcı bir betik eylemi olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dfd58-111">This command sets a previously successful script action to be a persisted script action.</span></span>

## <span data-ttu-id="dfd58-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dfd58-112">PARAMETERS</span></span>

### <span data-ttu-id="dfd58-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dfd58-113">-ClusterName</span></span>
<span data-ttu-id="dfd58-114">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfd58-114">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd58-115">-DefaultProfile</span></span>
<span data-ttu-id="dfd58-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dfd58-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd58-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfd58-117">-ResourceGroupName</span></span>
<span data-ttu-id="dfd58-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfd58-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd58-119">-Scriptexecutionıd</span><span class="sxs-lookup"><span data-stu-id="dfd58-119">-ScriptExecutionId</span></span>
<span data-ttu-id="dfd58-120">Kalıcı olarak yükseltilecek komut dosyası eyleminin yürütme KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfd58-120">Specifies the execution ID of the script action to promote to persisted.</span></span>
<span data-ttu-id="dfd58-121">Bu betik eyleminin yükseltilmesi için başarılı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dfd58-121">This script action must have succeeded in order to be promoted.</span></span>
<span data-ttu-id="dfd58-122">Get-AzureRmHDInsightScriptActionHistory kullanarak betik eylemi yürütme KIMLIĞINI bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dfd58-122">You can find the script action execution ID using Get-AzureRmHDInsightScriptActionHistory.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd58-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd58-123">CommonParameters</span></span>
<span data-ttu-id="dfd58-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dfd58-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd58-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd58-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd58-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dfd58-126">INPUTS</span></span>

### <span data-ttu-id="dfd58-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dfd58-127">None</span></span>
<span data-ttu-id="dfd58-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="dfd58-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dfd58-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dfd58-129">OUTPUTS</span></span>

### <span data-ttu-id="dfd58-130">System. void</span><span class="sxs-lookup"><span data-stu-id="dfd58-130">System.Void</span></span>

## <span data-ttu-id="dfd58-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dfd58-131">NOTES</span></span>

## <span data-ttu-id="dfd58-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dfd58-132">RELATED LINKS</span></span>

[<span data-ttu-id="dfd58-133">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="dfd58-133">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="dfd58-134">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="dfd58-134">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)


