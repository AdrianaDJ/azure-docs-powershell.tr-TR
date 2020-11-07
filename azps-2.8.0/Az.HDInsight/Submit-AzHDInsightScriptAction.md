---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: ef1c06c475b5de4984abf7859f033d68ad7d9dfa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751802"
---
# <span data-ttu-id="50cd3-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="50cd3-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="50cd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="50cd3-103">Bir Azure HDInsight kümesine yeni bir betik eylemi gönderir.</span><span class="sxs-lookup"><span data-stu-id="50cd3-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="50cd3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50cd3-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50cd3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="50cd3-105">DESCRIPTION</span></span>
<span data-ttu-id="50cd3-106">**Submit-AzHDInsightScriptAction** cmdlet 'ı bir Azure HDInsight kümesine yeni bir betik eylemi gönderir.</span><span class="sxs-lookup"><span data-stu-id="50cd3-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="50cd3-107">Komut dosyası eylemi ilk kez başarılı olduğu sürece, küme her ölçeklendiğinde betik eyleminin çalışması için *Persistonsuccess* 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="50cd3-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="50cd3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50cd3-108">EXAMPLES</span></span>

### <span data-ttu-id="50cd3-109">Örnek 1: çalışan bir HDInsight kümesine yeni bir betik eylemi gönderme</span><span class="sxs-lookup"><span data-stu-id="50cd3-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="50cd3-110">Bu komut, çalışan bir HDInsight kümesine bir betik eylemi gönderir.</span><span class="sxs-lookup"><span data-stu-id="50cd3-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="50cd3-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50cd3-111">PARAMETERS</span></span>

### <span data-ttu-id="50cd3-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="50cd3-112">-ApplicationName</span></span>
<span data-ttu-id="50cd3-113">Betik eyleminin uygulama adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50cd3-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="50cd3-114">*ApplicationName* belirtildiğinde, *persistonly* false olarak ayarlanmalıdır, düğümler yalnızca edgenode içermeli ve komut dosyası eylem sayısı 1 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="50cd3-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50cd3-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="50cd3-115">-ClusterName</span></span>
<span data-ttu-id="50cd3-116">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50cd3-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="50cd3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50cd3-117">-DefaultProfile</span></span>
<span data-ttu-id="50cd3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="50cd3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50cd3-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="50cd3-119">-Name</span></span>
<span data-ttu-id="50cd3-120">Betik eyleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50cd3-120">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50cd3-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="50cd3-121">-NodeTypes</span></span>
<span data-ttu-id="50cd3-122">Betik eyleminin çalıştırılacağı düğüm türlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50cd3-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50cd3-123">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="50cd3-123">-Parameters</span></span>
<span data-ttu-id="50cd3-124">Betik eyleminin parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50cd3-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50cd3-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="50cd3-125">-PersistOnSuccess</span></span>
<span data-ttu-id="50cd3-126">Küme her ölçeklendiğinde betik eyleminin çalışması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50cd3-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="50cd3-127">Komut dosyası eylemi ilk kez başarısız olursa bu Switch parametresi yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="50cd3-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50cd3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50cd3-128">-ResourceGroupName</span></span>
<span data-ttu-id="50cd3-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50cd3-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="50cd3-130">-URI</span><span class="sxs-lookup"><span data-stu-id="50cd3-130">-Uri</span></span>
<span data-ttu-id="50cd3-131">Betik eyleminin Genel URI 'sini (PowerShell veya bash betiği) belirtir.</span><span class="sxs-lookup"><span data-stu-id="50cd3-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50cd3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50cd3-132">CommonParameters</span></span>
<span data-ttu-id="50cd3-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50cd3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50cd3-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50cd3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50cd3-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50cd3-135">INPUTS</span></span>

### <span data-ttu-id="50cd3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="50cd3-136">System.String</span></span>

### <span data-ttu-id="50cd3-137">System. Uri</span><span class="sxs-lookup"><span data-stu-id="50cd3-137">System.Uri</span></span>

### <span data-ttu-id="50cd3-138">Microsoft. Azure. Commands. HDInsight. model. Management. RuntimeScriptActionClusterNodeType []</span><span class="sxs-lookup"><span data-stu-id="50cd3-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="50cd3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50cd3-139">OUTPUTS</span></span>

### <span data-ttu-id="50cd3-140">Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="50cd3-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="50cd3-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50cd3-141">NOTES</span></span>

## <span data-ttu-id="50cd3-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50cd3-142">RELATED LINKS</span></span>

[<span data-ttu-id="50cd3-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="50cd3-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)


