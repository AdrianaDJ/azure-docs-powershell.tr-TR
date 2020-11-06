---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 2a147e00dba480a483b10843b17347145a1dc2a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587692"
---
# <span data-ttu-id="52fe0-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="52fe0-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="52fe0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="52fe0-103">İşlem düğümünden RDP dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="52fe0-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52fe0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52fe0-104">SYNTAX</span></span>

### <span data-ttu-id="52fe0-105">Id_Path (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52fe0-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52fe0-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="52fe0-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52fe0-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="52fe0-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52fe0-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="52fe0-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52fe0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="52fe0-109">DESCRIPTION</span></span>
<span data-ttu-id="52fe0-110">**Get-AzureBatchRemoteDesktopProtocolFile** cmdlet 'i, bir Işlem düğümünden Uzak Masaüstü Protokolü (RDP) dosyası alır ve bunu dosya veya Kullanıcı tarafından sağlanan bir akışa kaydeder.</span><span class="sxs-lookup"><span data-stu-id="52fe0-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="52fe0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52fe0-111">EXAMPLES</span></span>

### <span data-ttu-id="52fe0-112">Örnek 1: belirtilen işlem düğümünden RDP dosyası alma ve dosyayı kaydetme</span><span class="sxs-lookup"><span data-stu-id="52fe0-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="52fe0-113">Bu komut, ComputeNode01 kimlik Pool06 olan havuzda KIMLIĞI olan bir RDP dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="52fe0-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="52fe0-114">Komut. rdp dosyasını C:\powershell\mycomputenode.rdpolarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="52fe0-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="52fe0-115">$Context değişkenine bağlam atamak için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="52fe0-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="52fe0-116">Örnek 2: bir işlem düğümünden RDP dosyası alın ve kanalı kullanarak dosyayı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="52fe0-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="52fe0-117">Bu komut, ComputeNode02 kimliğine sahip havuzda KIMLIK Pool06 olan COMPUTE düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="52fe0-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="52fe0-118">Komut bu işlem düğümünü ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="52fe0-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="52fe0-119">Geçerli cmdlet, COMPUTE düğümünden bir. rpd dosyası alır ve içeriği C:\powershell\mycomputenode02.rdpadlı bir dosya olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="52fe0-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="52fe0-120">Örnek 3: belirtilen işlem düğümünden RDP dosyası alın ve bunu bir akışa yönlendirin</span><span class="sxs-lookup"><span data-stu-id="52fe0-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="52fe0-121">İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="52fe0-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="52fe0-122">İkinci komut, KIMLIĞI Pool06 olan havuzda KIMLIK ComputeNode03 olan COMPUTE düğümünden bir. rdp dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="52fe0-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="52fe0-123">Komut dosya içeriğini $Stream akışa yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="52fe0-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="52fe0-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52fe0-124">PARAMETERS</span></span>

### <span data-ttu-id="52fe0-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="52fe0-125">-BatchContext</span></span>
<span data-ttu-id="52fe0-126">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52fe0-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="52fe0-127">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="52fe0-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="52fe0-128">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="52fe0-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="52fe0-129">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="52fe0-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="52fe0-130">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="52fe0-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52fe0-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="52fe0-131">-ComputeNode</span></span>
<span data-ttu-id="52fe0-132">**PSComputeNode** nesnesi olarak,. rdp dosyasının işaret ettiğini belirten bir COMPUTE düğümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52fe0-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="52fe0-133">Compute node nesnesi edinmek için Get-AzureBatchComputeNode cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="52fe0-133">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52fe0-134">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="52fe0-134">-ComputeNodeId</span></span>
<span data-ttu-id="52fe0-135">. Rdp dosyasının işaret olduğu COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="52fe0-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52fe0-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52fe0-136">-DefaultProfile</span></span>
<span data-ttu-id="52fe0-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52fe0-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52fe0-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="52fe0-138">-DestinationPath</span></span>
<span data-ttu-id="52fe0-139">Bu cmdlet 'in. rdp dosyasını kaydettiği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="52fe0-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fe0-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="52fe0-140">-DestinationStream</span></span>
<span data-ttu-id="52fe0-141">Bu cmdlet 'in RDP verilerini yönlendirdiği akışı belirtir.</span><span class="sxs-lookup"><span data-stu-id="52fe0-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="52fe0-142">Bu cmdlet bu akışı kapatmaz veya geri sarmaz.</span><span class="sxs-lookup"><span data-stu-id="52fe0-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52fe0-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="52fe0-143">-PoolId</span></span>
<span data-ttu-id="52fe0-144">Bu cmdlet 'in bir. rdp dosyası aldığı COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="52fe0-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52fe0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fe0-145">CommonParameters</span></span>
<span data-ttu-id="52fe0-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52fe0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fe0-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52fe0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fe0-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52fe0-148">INPUTS</span></span>

### <span data-ttu-id="52fe0-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="52fe0-149">BatchAccountContext</span></span>
<span data-ttu-id="52fe0-150">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="52fe0-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="52fe0-151">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="52fe0-151">PSComputeNode</span></span>
<span data-ttu-id="52fe0-152">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="52fe0-152">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="52fe0-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52fe0-153">OUTPUTS</span></span>

## <span data-ttu-id="52fe0-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52fe0-154">NOTES</span></span>

## <span data-ttu-id="52fe0-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52fe0-155">RELATED LINKS</span></span>

[<span data-ttu-id="52fe0-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="52fe0-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="52fe0-157">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="52fe0-157">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="52fe0-158">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="52fe0-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


