---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: 848f0cf3d2d36b9ff5c80792c23d126956dccfbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595028"
---
# <span data-ttu-id="76c89-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="76c89-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="76c89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76c89-102">SYNOPSIS</span></span>
<span data-ttu-id="76c89-103">İşlem düğümü için uzak oturum açma ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="76c89-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76c89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76c89-104">SYNTAX</span></span>

### <span data-ttu-id="76c89-105">Kimlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76c89-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76c89-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="76c89-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76c89-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="76c89-107">DESCRIPTION</span></span>
<span data-ttu-id="76c89-108">**Get-AzureBatchRemoteLoginSettings** cmdlet 'i, sanal makine altyapısına dayalı havuzda bir hesaplama düğümü için uzaktan oturum açma ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="76c89-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="76c89-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76c89-109">EXAMPLES</span></span>

### <span data-ttu-id="76c89-110">Örnek 1: havuzdaki tüm düğümler için uzaktan oturum açma ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="76c89-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="76c89-111">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak aboneliğinizin erişim tuşlarını içeren bir toplu hesap bağlamını alır.</span><span class="sxs-lookup"><span data-stu-id="76c89-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="76c89-112">Komut, $Context değişkeninde bağlamı depolar ve sonraki komutta kullanılır.</span><span class="sxs-lookup"><span data-stu-id="76c89-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="76c89-113">İkinci komut, **Get-AzureBatchComputeNode** kullanarak havuzdaki tüm COMPUTE düğümünü</span><span class="sxs-lookup"><span data-stu-id="76c89-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="76c89-114">Komut, ardışık düzen işlecini kullanarak her bilgisayar düğümünü geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="76c89-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="76c89-115">Komut, her işlem düğümü için uzak oturum açma ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="76c89-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="76c89-116">Örnek 2: düğüm için uzak oturum açma ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="76c89-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="76c89-117">İlk komut, aboneliğinizin erişim tuşlarını içeren bir toplu hesap bağlamını alır ve $Context değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="76c89-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>

<span data-ttu-id="76c89-118">İkinci komut, KIMLIĞI etkileyen havuzda bulunan havuzda belirtilen KIMLIĞINE sahip olan COMPUTE düğümü için uzaktan oturum açma ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="76c89-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="76c89-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76c89-119">PARAMETERS</span></span>

### <span data-ttu-id="76c89-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="76c89-120">-BatchContext</span></span>
<span data-ttu-id="76c89-121">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c89-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="76c89-122">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="76c89-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="76c89-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="76c89-123">-ComputeNode</span></span>
<span data-ttu-id="76c89-124">Bu cmdlet 'in uzaktan oturum açma ayarlarını aldığı **PSComputeNode** nesnesi olarak bir COMPUTE düğümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c89-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="76c89-125">Compute node nesnesi edinmek için Get-AzureBatchComputeNode cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="76c89-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="76c89-126">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="76c89-126">-ComputeNodeId</span></span>
<span data-ttu-id="76c89-127">Uzaktan oturum açma ayarlarının alınacağı işlem düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c89-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="76c89-128">Bu cmdlet 'in uzaktan oturum açma ayarlarını aldığı.</span><span class="sxs-lookup"><span data-stu-id="76c89-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="76c89-129">-PoolId</span><span class="sxs-lookup"><span data-stu-id="76c89-129">-PoolId</span></span>
<span data-ttu-id="76c89-130">Sanal makineyi içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="76c89-130">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="76c89-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c89-131">-DefaultProfile</span></span>
<span data-ttu-id="76c89-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76c89-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76c89-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c89-133">CommonParameters</span></span>
<span data-ttu-id="76c89-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76c89-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c89-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c89-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c89-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76c89-136">INPUTS</span></span>

### <span data-ttu-id="76c89-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="76c89-137">BatchAccountContext</span></span>
<span data-ttu-id="76c89-138">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="76c89-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="76c89-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="76c89-139">PSComputeNode</span></span>
<span data-ttu-id="76c89-140">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="76c89-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="76c89-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76c89-141">OUTPUTS</span></span>

### <span data-ttu-id="76c89-142">PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="76c89-142">PSRemoteLoginSettings</span></span>

## <span data-ttu-id="76c89-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76c89-143">NOTES</span></span>

## <span data-ttu-id="76c89-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76c89-144">RELATED LINKS</span></span>

[<span data-ttu-id="76c89-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="76c89-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="76c89-146">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="76c89-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="76c89-147">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="76c89-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="76c89-148">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="76c89-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


