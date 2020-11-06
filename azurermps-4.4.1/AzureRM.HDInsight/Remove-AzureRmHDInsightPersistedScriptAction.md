---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 28526dd4aaa36890800a2bffd47eeae3f281d747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587932"
---
# <span data-ttu-id="f1524-101">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f1524-101">Remove-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="f1524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1524-102">SYNOPSIS</span></span>
<span data-ttu-id="f1524-103">Bir HDInsight kümesinden kalıcı betik eylemini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f1524-103">Removes an persisted script action from an HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1524-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1524-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1524-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1524-105">DESCRIPTION</span></span>
<span data-ttu-id="f1524-106">**Remove-AzureRmHDInsightPersistedScriptAction** cmdlet 'i, belirtilen Azure HDInsight kümesinin kalıcı betik eylemleri listesinden kalıcı bir betik eylemini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f1524-106">The **Remove-AzureRmHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="f1524-107">Kaldırılan betik, küme ölçeklendiğinde artık yürütülmez.</span><span class="sxs-lookup"><span data-stu-id="f1524-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="f1524-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1524-108">EXAMPLES</span></span>

### <span data-ttu-id="f1524-109">Örnek 1: bir kümedeki kalıcı betik eylemleri listesinden bir betik eylemini kaldırma</span><span class="sxs-lookup"><span data-stu-id="f1524-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="f1524-110">Bu komut ScriptAction adlı betik eylemini belirtilen kümedeki kalıcı betik eylemleri listesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f1524-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="f1524-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1524-111">PARAMETERS</span></span>

### <span data-ttu-id="f1524-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f1524-112">-ClusterName</span></span>
<span data-ttu-id="f1524-113">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1524-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f1524-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1524-114">-Name</span></span>
<span data-ttu-id="f1524-115">Kaldırılacak olan kalıcı betik eyleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1524-115">Specifies the name of the persisted script action to be removed.</span></span>

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

### <span data-ttu-id="f1524-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1524-116">-ResourceGroupName</span></span>
<span data-ttu-id="f1524-117">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1524-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f1524-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1524-118">-DefaultProfile</span></span>
<span data-ttu-id="f1524-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1524-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1524-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1524-120">CommonParameters</span></span>
<span data-ttu-id="f1524-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1524-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1524-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1524-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1524-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1524-123">INPUTS</span></span>

## <span data-ttu-id="f1524-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1524-124">OUTPUTS</span></span>

### <span data-ttu-id="f1524-125">System. void</span><span class="sxs-lookup"><span data-stu-id="f1524-125">System.Void</span></span>

## <span data-ttu-id="f1524-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1524-126">NOTES</span></span>

## <span data-ttu-id="f1524-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1524-127">RELATED LINKS</span></span>

[<span data-ttu-id="f1524-128">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f1524-128">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="f1524-129">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="f1524-129">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


