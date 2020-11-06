---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 37d91dc6fd9d90291c7b619fdb9839d6d9af83b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595031"
---
# <span data-ttu-id="89f29-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="89f29-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="89f29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89f29-102">SYNOPSIS</span></span>
<span data-ttu-id="89f29-103">İşlem düğümünden RDP dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="89f29-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89f29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89f29-104">SYNTAX</span></span>

### <span data-ttu-id="89f29-105">Id_Path (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89f29-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89f29-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="89f29-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89f29-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="89f29-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89f29-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="89f29-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89f29-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="89f29-109">DESCRIPTION</span></span>
<span data-ttu-id="89f29-110">**Get-AzureBatchRemoteDesktopProtocolFile** cmdlet 'i, bir Işlem düğümünden Uzak Masaüstü Protokolü (RDP) dosyası alır ve bunu dosya veya Kullanıcı tarafından sağlanan bir akışa kaydeder.</span><span class="sxs-lookup"><span data-stu-id="89f29-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="89f29-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89f29-111">EXAMPLES</span></span>

### <span data-ttu-id="89f29-112">Örnek 1: belirtilen işlem düğümünden RDP dosyası alma ve dosyayı kaydetme</span><span class="sxs-lookup"><span data-stu-id="89f29-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="89f29-113">Bu komut, ComputeNode01 kimlik Pool06 olan havuzda KIMLIĞI olan bir RDP dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="89f29-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="89f29-114">Komut. rdp dosyasını C:\powershell\mycomputenode.rdpolarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="89f29-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="89f29-115">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="89f29-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="89f29-116">Örnek 2: bir işlem düğümünden RDP dosyası alın ve kanalı kullanarak dosyayı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="89f29-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="89f29-117">Bu komut, ComputeNode02 kimliğine sahip havuzda KIMLIK Pool06 olan COMPUTE düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="89f29-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="89f29-118">Komut bu işlem düğümünü ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="89f29-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="89f29-119">Geçerli cmdlet, COMPUTE düğümünden bir. rpd dosyası alır ve içeriği C:\powershell\mycomputenode02.rdpadlı bir dosya olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="89f29-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="89f29-120">Örnek 3: belirtilen işlem düğümünden RDP dosyası alın ve bunu bir akışa yönlendirin</span><span class="sxs-lookup"><span data-stu-id="89f29-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="89f29-121">İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="89f29-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="89f29-122">İkinci komut, KIMLIĞI Pool06 olan havuzda KIMLIK ComputeNode03 olan COMPUTE düğümünden bir. rdp dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="89f29-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="89f29-123">Komut dosya içeriğini $Stream akışa yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="89f29-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="89f29-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89f29-124">PARAMETERS</span></span>

### <span data-ttu-id="89f29-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="89f29-125">-BatchContext</span></span>
<span data-ttu-id="89f29-126">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="89f29-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="89f29-127">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="89f29-127">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="89f29-128">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="89f29-128">-ComputeNode</span></span>
<span data-ttu-id="89f29-129">**PSComputeNode** nesnesi olarak,. rdp dosyasının işaret ettiğini belirten bir COMPUTE düğümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="89f29-129">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="89f29-130">Compute node nesnesi edinmek için Get-AzureBatchComputeNode cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="89f29-130">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89f29-131">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="89f29-131">-ComputeNodeId</span></span>
<span data-ttu-id="89f29-132">. Rdp dosyasının işaret olduğu COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="89f29-132">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f29-133">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="89f29-133">-DestinationPath</span></span>
<span data-ttu-id="89f29-134">Bu cmdlet 'in. rdp dosyasını kaydettiği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="89f29-134">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f29-135">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="89f29-135">-DestinationStream</span></span>
<span data-ttu-id="89f29-136">Bu cmdlet 'in RDP verilerini yönlendirdiği akışı belirtir.</span><span class="sxs-lookup"><span data-stu-id="89f29-136">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="89f29-137">Bu cmdlet bu akışı kapatmaz veya geri sarmaz.</span><span class="sxs-lookup"><span data-stu-id="89f29-137">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89f29-138">-PoolId</span><span class="sxs-lookup"><span data-stu-id="89f29-138">-PoolId</span></span>
<span data-ttu-id="89f29-139">Bu cmdlet 'in bir. rdp dosyası aldığı COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="89f29-139">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89f29-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89f29-140">-DefaultProfile</span></span>
<span data-ttu-id="89f29-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89f29-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89f29-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89f29-142">CommonParameters</span></span>
<span data-ttu-id="89f29-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89f29-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89f29-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89f29-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89f29-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89f29-145">INPUTS</span></span>

### <span data-ttu-id="89f29-146">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="89f29-146">BatchAccountContext</span></span>
<span data-ttu-id="89f29-147">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="89f29-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="89f29-148">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="89f29-148">PSComputeNode</span></span>
<span data-ttu-id="89f29-149">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="89f29-149">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="89f29-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89f29-150">OUTPUTS</span></span>

## <span data-ttu-id="89f29-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89f29-151">NOTES</span></span>

## <span data-ttu-id="89f29-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89f29-152">RELATED LINKS</span></span>

[<span data-ttu-id="89f29-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="89f29-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="89f29-154">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="89f29-154">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="89f29-155">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="89f29-155">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


