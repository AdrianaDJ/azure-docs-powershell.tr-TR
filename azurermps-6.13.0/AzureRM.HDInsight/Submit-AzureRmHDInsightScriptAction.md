---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 884741f6543dee05ed8236385071ad345321413e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590255"
---
# <span data-ttu-id="cf789-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="cf789-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="cf789-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf789-102">SYNOPSIS</span></span>
<span data-ttu-id="cf789-103">Bir Azure HDInsight kümesine yeni bir betik eylemi gönderir.</span><span class="sxs-lookup"><span data-stu-id="cf789-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf789-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf789-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf789-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf789-105">DESCRIPTION</span></span>
<span data-ttu-id="cf789-106">**Submit-AzureRmHDInsightScriptAction** cmdlet 'ı bir Azure HDInsight kümesine yeni bir betik eylemi gönderir.</span><span class="sxs-lookup"><span data-stu-id="cf789-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="cf789-107">Komut dosyası eylemi ilk kez başarılı olduğu sürece, küme her ölçeklendiğinde betik eyleminin çalışması için *Persistonsuccess* 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="cf789-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="cf789-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf789-108">EXAMPLES</span></span>

### <span data-ttu-id="cf789-109">Örnek 1: çalışan bir HDInsight kümesine yeni bir betik eylemi gönderme</span><span class="sxs-lookup"><span data-stu-id="cf789-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="cf789-110">Bu komut, çalışan bir HDInsight kümesine bir betik eylemi gönderir.</span><span class="sxs-lookup"><span data-stu-id="cf789-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="cf789-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf789-111">PARAMETERS</span></span>

### <span data-ttu-id="cf789-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="cf789-112">-ApplicationName</span></span>
<span data-ttu-id="cf789-113">Betik eyleminin uygulama adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf789-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="cf789-114">*ApplicationName* belirtildiğinde, *persistonly* false olarak ayarlanmalıdır, düğümler yalnızca edgenode içermeli ve komut dosyası eylem sayısı 1 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cf789-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

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

### <span data-ttu-id="cf789-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cf789-115">-ClusterName</span></span>
<span data-ttu-id="cf789-116">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf789-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="cf789-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf789-117">-DefaultProfile</span></span>
<span data-ttu-id="cf789-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cf789-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf789-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="cf789-119">-Name</span></span>
<span data-ttu-id="cf789-120">Betik eyleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf789-120">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="cf789-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="cf789-121">-NodeTypes</span></span>
<span data-ttu-id="cf789-122">Betik eyleminin çalıştırılacağı düğüm türlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf789-122">Specifies the node types on which to run the script action.</span></span>

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

### <span data-ttu-id="cf789-123">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="cf789-123">-Parameters</span></span>
<span data-ttu-id="cf789-124">Betik eyleminin parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf789-124">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="cf789-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="cf789-125">-PersistOnSuccess</span></span>
<span data-ttu-id="cf789-126">Küme her ölçeklendiğinde betik eyleminin çalışması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf789-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="cf789-127">Komut dosyası eylemi ilk kez başarısız olursa bu Switch parametresi yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="cf789-127">This switch parameter is ignored if the script action initially fails.</span></span>

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

### <span data-ttu-id="cf789-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf789-128">-ResourceGroupName</span></span>
<span data-ttu-id="cf789-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf789-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cf789-130">-URI</span><span class="sxs-lookup"><span data-stu-id="cf789-130">-Uri</span></span>
<span data-ttu-id="cf789-131">Betik eyleminin Genel URI 'sini (PowerShell veya bash betiği) belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf789-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="cf789-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf789-132">CommonParameters</span></span>
<span data-ttu-id="cf789-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf789-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf789-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf789-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf789-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf789-135">INPUTS</span></span>

### <span data-ttu-id="cf789-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cf789-136">System.String</span></span>

### <span data-ttu-id="cf789-137">System. Uri</span><span class="sxs-lookup"><span data-stu-id="cf789-137">System.Uri</span></span>

### <span data-ttu-id="cf789-138">Microsoft. Azure. Commands. HDInsight. model. Management. RuntimeScriptActionClusterNodeType []</span><span class="sxs-lookup"><span data-stu-id="cf789-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="cf789-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf789-139">OUTPUTS</span></span>

### <span data-ttu-id="cf789-140">Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="cf789-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="cf789-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf789-141">NOTES</span></span>

## <span data-ttu-id="cf789-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf789-142">RELATED LINKS</span></span>

[<span data-ttu-id="cf789-143">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="cf789-143">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


