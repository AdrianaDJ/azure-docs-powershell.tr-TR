---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 03c37bb1cf70dfefc5373e9211d6365feb133ad4
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761870"
---
# <span data-ttu-id="928cc-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="928cc-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="928cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="928cc-102">SYNOPSIS</span></span>
<span data-ttu-id="928cc-103">İşlem düğümü için uzak oturum açma ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="928cc-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="928cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="928cc-104">SYNTAX</span></span>

### <span data-ttu-id="928cc-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="928cc-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="928cc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="928cc-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="928cc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="928cc-107">DESCRIPTION</span></span>
<span data-ttu-id="928cc-108">**Get-AzBatchRemoteLoginSetting** cmdlet 'i, sanal makine altyapısına dayalı havuzda bir hesaplama düğümü için uzaktan oturum açma ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="928cc-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="928cc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="928cc-109">EXAMPLES</span></span>

### <span data-ttu-id="928cc-110">Örnek 1: havuzdaki tüm düğümler için uzaktan oturum açma ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="928cc-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="928cc-111">İlk komut, **Get-AzBatchAccountKeys** kullanarak aboneliğinizin erişim tuşlarını içeren bir toplu hesap bağlamı alır.</span><span class="sxs-lookup"><span data-stu-id="928cc-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="928cc-112">Komut, $Context değişkeninde bağlamı depolar ve sonraki komutta kullanılır.</span><span class="sxs-lookup"><span data-stu-id="928cc-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="928cc-113">İkinci komut, **Get-AzBatchComputeNode** kullanarak havuzdaki tüm COMPUTE düğümünü</span><span class="sxs-lookup"><span data-stu-id="928cc-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="928cc-114">Komut, ardışık düzen işlecini kullanarak her bilgisayar düğümünü geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="928cc-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="928cc-115">Komut, her işlem düğümü için uzak oturum açma ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="928cc-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="928cc-116">Örnek 2: düğüm için uzak oturum açma ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="928cc-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="928cc-117">İlk komut, aboneliğinizin erişim tuşlarını içeren bir toplu hesap bağlamını alır ve $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="928cc-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="928cc-118">İkinci komut, KIMLIĞI etkileyen havuzda bulunan havuzda belirtilen KIMLIĞINE sahip olan COMPUTE düğümü için uzaktan oturum açma ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="928cc-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="928cc-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="928cc-119">PARAMETERS</span></span>

### <span data-ttu-id="928cc-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="928cc-120">-BatchContext</span></span>
<span data-ttu-id="928cc-121">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="928cc-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="928cc-122">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** edinmek için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="928cc-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="928cc-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="928cc-123">-ComputeNode</span></span>
<span data-ttu-id="928cc-124">Bu cmdlet 'in uzaktan oturum açma ayarlarını aldığı **PSComputeNode** nesnesi olarak bir COMPUTE düğümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="928cc-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="928cc-125">Compute node nesnesi edinmek için Get-AzBatchComputeNode cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="928cc-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="928cc-126">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="928cc-126">-ComputeNodeId</span></span>
<span data-ttu-id="928cc-127">Uzaktan oturum açma ayarlarının alınacağı işlem düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="928cc-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="928cc-128">Bu cmdlet 'in uzaktan oturum açma ayarlarını aldığı.</span><span class="sxs-lookup"><span data-stu-id="928cc-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928cc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928cc-129">-DefaultProfile</span></span>
<span data-ttu-id="928cc-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="928cc-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="928cc-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="928cc-131">-PoolId</span></span>
<span data-ttu-id="928cc-132">Sanal makineyi içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="928cc-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928cc-133">CommonParameters</span></span>
<span data-ttu-id="928cc-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="928cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928cc-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928cc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928cc-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="928cc-136">INPUTS</span></span>

### <span data-ttu-id="928cc-137">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="928cc-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="928cc-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="928cc-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="928cc-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="928cc-139">OUTPUTS</span></span>

### <span data-ttu-id="928cc-140">Microsoft.Azure.Commands.Batch. Modeller. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="928cc-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="928cc-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="928cc-141">NOTES</span></span>

## <span data-ttu-id="928cc-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="928cc-142">RELATED LINKS</span></span>

[<span data-ttu-id="928cc-143">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="928cc-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="928cc-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="928cc-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="928cc-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="928cc-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="928cc-146">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="928cc-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


