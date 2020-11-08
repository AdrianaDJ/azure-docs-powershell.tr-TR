---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: 56ec7eafcea7233697089d692b2799fa6c9b744a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098480"
---
# <span data-ttu-id="076cd-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="076cd-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="076cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="076cd-102">SYNOPSIS</span></span>
<span data-ttu-id="076cd-103">Toplu hesap için desteklenen toplu Iş görüntülerini alır.</span><span class="sxs-lookup"><span data-stu-id="076cd-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="076cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="076cd-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="076cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="076cd-105">DESCRIPTION</span></span>
<span data-ttu-id="076cd-106">**Get-AzBatchSupportedImage** cmdlet 'ı, Azure toplu hesabında kullanılabilen desteklenen sanal makine görüntülerini alır.</span><span class="sxs-lookup"><span data-stu-id="076cd-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="076cd-107">*Batchcontext* parametresini kullanarak hesabı belirtin.</span><span class="sxs-lookup"><span data-stu-id="076cd-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="076cd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="076cd-108">EXAMPLES</span></span>

### <span data-ttu-id="076cd-109">Örnek 1: kullanılabilir tüm desteklenen resimleri alma</span><span class="sxs-lookup"><span data-stu-id="076cd-109">Example 1: Get all available supported images</span></span>

```powershell
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchSupportedImage -BatchContext $Context
BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:16.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 16.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:18.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 18.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : credativ:debian:8:latest
NodeAgentSkuId        : batch.node.debian 8
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : microsoftwindowsserver:windowsserver:2016-datacenter:latest
NodeAgentSkuId        : batch.node.windows amd64
OSType                : Windows
VerificationType      : Verified

...
```

<span data-ttu-id="076cd-110">İlk komut, **Get-AzBatchAccountKey** kullanarak aboneliğinizin erişim tuşlarını Içeren bir toplu hesap bağlamını alır.</span><span class="sxs-lookup"><span data-stu-id="076cd-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="076cd-111">Komut, $Context değişkeninde bağlamı depolar ve sonraki komutta kullanılır.</span><span class="sxs-lookup"><span data-stu-id="076cd-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="076cd-112">İkinci komut, bu toplu hesap için sağlanan tüm desteklenen resimleri alır.</span><span class="sxs-lookup"><span data-stu-id="076cd-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="076cd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="076cd-113">PARAMETERS</span></span>

### <span data-ttu-id="076cd-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="076cd-114">-BatchContext</span></span>
<span data-ttu-id="076cd-115">Toplu Iş hizmetiyle etkileşim kurarken kullanılacak BatchAccountContext örneği.</span><span class="sxs-lookup"><span data-stu-id="076cd-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="076cd-116">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="076cd-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="076cd-117">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="076cd-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="076cd-118">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="076cd-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="076cd-119">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="076cd-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="076cd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="076cd-120">-DefaultProfile</span></span>
<span data-ttu-id="076cd-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="076cd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076cd-122">-Filtre</span><span class="sxs-lookup"><span data-stu-id="076cd-122">-Filter</span></span>
<span data-ttu-id="076cd-123">Desteklenen resimler için bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="076cd-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="076cd-124">Filtre belirtmezseniz, bu cmdlet toplu hesabın desteklediği tüm resimleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="076cd-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

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

### <span data-ttu-id="076cd-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="076cd-125">-MaxCount</span></span>
<span data-ttu-id="076cd-126">Döndürülecek en fazla desteklenen resim sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="076cd-126">Specifies the maximum number of supported images to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="076cd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="076cd-127">CommonParameters</span></span>
<span data-ttu-id="076cd-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="076cd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="076cd-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="076cd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="076cd-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="076cd-130">INPUTS</span></span>

### <span data-ttu-id="076cd-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="076cd-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="076cd-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="076cd-132">OUTPUTS</span></span>

### <span data-ttu-id="076cd-133">Microsoft.Azure.Commands.Batch. Modeller. daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="076cd-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="076cd-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="076cd-134">NOTES</span></span>

## <span data-ttu-id="076cd-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="076cd-135">RELATED LINKS</span></span>
[<span data-ttu-id="076cd-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="076cd-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)