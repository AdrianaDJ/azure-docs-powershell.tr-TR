---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 6ed0fca41dff56da768da33892b7960f639eb91c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107218"
---
# <span data-ttu-id="0f489-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="0f489-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="0f489-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f489-102">SYNOPSIS</span></span>
<span data-ttu-id="0f489-103">İşlem düğümünden RDP dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="0f489-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="0f489-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f489-104">SYNTAX</span></span>

### <span data-ttu-id="0f489-105">Id_Path (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f489-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f489-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="0f489-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f489-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="0f489-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f489-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="0f489-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f489-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f489-109">DESCRIPTION</span></span>
<span data-ttu-id="0f489-110">**Get-AzBatchRemoteDesktopProtocolFile** cmdlet 'i, bir Işlem düğümünden Uzak Masaüstü Protokolü (RDP) dosyası alır ve bunu dosya veya Kullanıcı tarafından sağlanan bir akışa kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0f489-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="0f489-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f489-111">EXAMPLES</span></span>

### <span data-ttu-id="0f489-112">Örnek 1: belirtilen işlem düğümünden RDP dosyası alma ve dosyayı kaydetme</span><span class="sxs-lookup"><span data-stu-id="0f489-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="0f489-113">Bu komut, ComputeNode01 kimlik Pool06 olan havuzda KIMLIĞI olan bir RDP dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="0f489-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="0f489-114">Komut. rdp dosyasını C:\powershell\mycomputenode.rdpolarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0f489-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="0f489-115">$Context değişkenine bağlam atamak için Get-AzBatchAccountKey cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0f489-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0f489-116">Örnek 2: bir işlem düğümünden RDP dosyası alın ve kanalı kullanarak dosyayı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="0f489-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="0f489-117">Bu komut, ComputeNode02 kimliğine sahip havuzda KIMLIK Pool06 olan COMPUTE düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="0f489-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="0f489-118">Komut bu işlem düğümünü ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="0f489-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0f489-119">Geçerli cmdlet, COMPUTE düğümünden bir. rpd dosyası alır ve içeriği C:\powershell\mycomputenode02.rdpadlı bir dosya olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0f489-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="0f489-120">Örnek 3: belirtilen işlem düğümünden RDP dosyası alın ve bunu bir akışa yönlendirin</span><span class="sxs-lookup"><span data-stu-id="0f489-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="0f489-121">İlk komut New-Object cmdlet 'ini kullanarak bir akış oluşturur ve $Stream değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0f489-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="0f489-122">İkinci komut, KIMLIĞI Pool06 olan havuzda KIMLIK ComputeNode03 olan COMPUTE düğümünden bir. rdp dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="0f489-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="0f489-123">Komut dosya içeriğini $Stream akışa yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="0f489-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="0f489-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f489-124">PARAMETERS</span></span>

### <span data-ttu-id="0f489-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0f489-125">-BatchContext</span></span>
<span data-ttu-id="0f489-126">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f489-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0f489-127">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0f489-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0f489-128">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="0f489-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0f489-129">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0f489-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0f489-130">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0f489-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0f489-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="0f489-131">-ComputeNode</span></span>
<span data-ttu-id="0f489-132">**PSComputeNode** nesnesi olarak,. rdp dosyasının işaret ettiğini belirten bir COMPUTE düğümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f489-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="0f489-133">Compute node nesnesi edinmek için Get-AzBatchComputeNode cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0f489-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="0f489-134">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="0f489-134">-ComputeNodeId</span></span>
<span data-ttu-id="0f489-135">. Rdp dosyasının işaret olduğu COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f489-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="0f489-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f489-136">-DefaultProfile</span></span>
<span data-ttu-id="0f489-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f489-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f489-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="0f489-138">-DestinationPath</span></span>
<span data-ttu-id="0f489-139">Bu cmdlet 'in. rdp dosyasını kaydettiği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f489-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="0f489-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="0f489-140">-DestinationStream</span></span>
<span data-ttu-id="0f489-141">Bu cmdlet 'in RDP verilerini yönlendirdiği akışı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f489-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="0f489-142">Bu cmdlet bu akışı kapatmaz veya geri sarmaz.</span><span class="sxs-lookup"><span data-stu-id="0f489-142">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="0f489-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="0f489-143">-PoolId</span></span>
<span data-ttu-id="0f489-144">Bu cmdlet 'in bir. rdp dosyası aldığı COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f489-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="0f489-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f489-145">CommonParameters</span></span>
<span data-ttu-id="0f489-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f489-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f489-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0f489-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f489-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f489-148">INPUTS</span></span>

### <span data-ttu-id="0f489-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0f489-149">System.String</span></span>

### <span data-ttu-id="0f489-150">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="0f489-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="0f489-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0f489-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0f489-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f489-152">OUTPUTS</span></span>

### <span data-ttu-id="0f489-153">System. void</span><span class="sxs-lookup"><span data-stu-id="0f489-153">System.Void</span></span>

## <span data-ttu-id="0f489-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f489-154">NOTES</span></span>

## <span data-ttu-id="0f489-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f489-155">RELATED LINKS</span></span>

[<span data-ttu-id="0f489-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0f489-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="0f489-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="0f489-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="0f489-158">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="0f489-158">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


