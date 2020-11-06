---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 866bd8c8189ca727b3893f09370bcca1136e827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594484"
---
# <span data-ttu-id="5db2f-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="5db2f-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="5db2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5db2f-102">SYNOPSIS</span></span>
<span data-ttu-id="5db2f-103">Bir Azure HDInsight kümesine yeni bir betik eylemi gönderir.</span><span class="sxs-lookup"><span data-stu-id="5db2f-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5db2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5db2f-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5db2f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5db2f-105">DESCRIPTION</span></span>
<span data-ttu-id="5db2f-106">**Submit-AzureRmHDInsightScriptAction** cmdlet 'ı bir Azure HDInsight kümesine yeni bir betik eylemi gönderir.</span><span class="sxs-lookup"><span data-stu-id="5db2f-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="5db2f-107">Komut dosyası eylemi ilk kez başarılı olduğu sürece, küme her ölçeklendiğinde betik eyleminin çalışması için *Persistonsuccess* 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5db2f-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="5db2f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5db2f-108">EXAMPLES</span></span>

### <span data-ttu-id="5db2f-109">Örnek 1: çalışan bir HDInsight kümesine yeni bir betik eylemi gönderme</span><span class="sxs-lookup"><span data-stu-id="5db2f-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="5db2f-110">Bu komut, çalışan bir HDInsight kümesine bir betik eylemi gönderir.</span><span class="sxs-lookup"><span data-stu-id="5db2f-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="5db2f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5db2f-111">PARAMETERS</span></span>

### <span data-ttu-id="5db2f-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="5db2f-112">-ApplicationName</span></span>
<span data-ttu-id="5db2f-113">Betik eyleminin uygulama adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5db2f-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="5db2f-114">*ApplicationName* belirtildiğinde, *persistonly* false olarak ayarlanmalıdır, düğümler yalnızca edgenode içermeli ve komut dosyası eylem sayısı 1 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5db2f-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5db2f-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5db2f-115">-ClusterName</span></span>
<span data-ttu-id="5db2f-116">Kümenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5db2f-116">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5db2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db2f-117">-DefaultProfile</span></span>
<span data-ttu-id="5db2f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5db2f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5db2f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5db2f-119">-Name</span></span>
<span data-ttu-id="5db2f-120">Betik eyleminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5db2f-120">Specifies the name of the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5db2f-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="5db2f-121">-NodeTypes</span></span>
<span data-ttu-id="5db2f-122">Betik eyleminin çalıştırılacağı düğüm türlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5db2f-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5db2f-123">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="5db2f-123">-Parameters</span></span>
<span data-ttu-id="5db2f-124">Betik eyleminin parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5db2f-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5db2f-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="5db2f-125">-PersistOnSuccess</span></span>
<span data-ttu-id="5db2f-126">Küme her ölçeklendiğinde betik eyleminin çalışması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5db2f-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="5db2f-127">Komut dosyası eylemi ilk kez başarısız olursa bu Switch parametresi yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="5db2f-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db2f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db2f-128">-ResourceGroupName</span></span>
<span data-ttu-id="5db2f-129">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5db2f-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5db2f-130">-URI</span><span class="sxs-lookup"><span data-stu-id="5db2f-130">-Uri</span></span>
<span data-ttu-id="5db2f-131">Betik eyleminin Genel URI 'sini (PowerShell veya bash betiği) belirtir.</span><span class="sxs-lookup"><span data-stu-id="5db2f-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5db2f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db2f-132">CommonParameters</span></span>
<span data-ttu-id="5db2f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5db2f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db2f-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5db2f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db2f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5db2f-135">INPUTS</span></span>

### <span data-ttu-id="5db2f-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5db2f-136">None</span></span>
<span data-ttu-id="5db2f-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5db2f-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5db2f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5db2f-138">OUTPUTS</span></span>

### <span data-ttu-id="5db2f-139">Microsoft. Azure. Commands. HDInsight. model. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="5db2f-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="5db2f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5db2f-140">NOTES</span></span>

## <span data-ttu-id="5db2f-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5db2f-141">RELATED LINKS</span></span>

[<span data-ttu-id="5db2f-142">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="5db2f-142">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


