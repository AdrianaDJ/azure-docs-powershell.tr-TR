---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: 86451c1ac7ba52c9b013b3724d9c706caaa961ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572930"
---
# <span data-ttu-id="af0c2-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="af0c2-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="af0c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="af0c2-103">Toplu iş hesabındaki toplu Iş düğümü Aracısı SKU 'Larını alır.</span><span class="sxs-lookup"><span data-stu-id="af0c2-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af0c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af0c2-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af0c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="af0c2-105">DESCRIPTION</span></span>
<span data-ttu-id="af0c2-106">**Get-AzureBatchNodeAgentSku** cmdlet 'ı bir Azure toplu hesabında kullanılabilen düğüm Aracısı SKU 'larını alır.</span><span class="sxs-lookup"><span data-stu-id="af0c2-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="af0c2-107">*Batchcontext* parametresini kullanarak hesabı belirtin.</span><span class="sxs-lookup"><span data-stu-id="af0c2-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="af0c2-108">Aramanızı açık bir veri Protokolü (OData) filtresiyle eşleşen STB 'ler olarak daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af0c2-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="af0c2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af0c2-109">EXAMPLES</span></span>

### <span data-ttu-id="af0c2-110">Örnek 1: tüm kullanılabilir düğüm Aracısı SKU 'Larını alma</span><span class="sxs-lookup"><span data-stu-id="af0c2-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="af0c2-111">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak aboneliğinizin erişim tuşlarını içeren bir toplu hesap bağlamını alır.</span><span class="sxs-lookup"><span data-stu-id="af0c2-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="af0c2-112">Komut, $Context değişkeninde bağlamı depolar ve sonraki komutta kullanılır.</span><span class="sxs-lookup"><span data-stu-id="af0c2-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="af0c2-113">İkinci komut, toplu Iş desteği olan tüm kullanılabilir düğüm Aracısı SKU 'Larını alır.</span><span class="sxs-lookup"><span data-stu-id="af0c2-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="af0c2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af0c2-114">PARAMETERS</span></span>

### <span data-ttu-id="af0c2-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="af0c2-115">-BatchContext</span></span>
<span data-ttu-id="af0c2-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="af0c2-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="af0c2-117">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="af0c2-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="af0c2-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="af0c2-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="af0c2-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="af0c2-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="af0c2-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="af0c2-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="af0c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af0c2-121">-DefaultProfile</span></span>
<span data-ttu-id="af0c2-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af0c2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af0c2-123">-Filtre</span><span class="sxs-lookup"><span data-stu-id="af0c2-123">-Filter</span></span>
<span data-ttu-id="af0c2-124">Düğüm Aracısı SKU 'Ları için bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="af0c2-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="af0c2-125">Filtre belirtmezseniz, bu cmdlet toplu Işlemle desteklenen tüm düğüm Aracısı SKU 'Larını döndürür.</span><span class="sxs-lookup"><span data-stu-id="af0c2-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="af0c2-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="af0c2-126">-MaxCount</span></span>
<span data-ttu-id="af0c2-127">Döndürülecek düğüm Aracısı SKU sayısının üst sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af0c2-127">Specifies the maximum number of node agent SKUs to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af0c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af0c2-128">CommonParameters</span></span>
<span data-ttu-id="af0c2-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af0c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af0c2-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af0c2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af0c2-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af0c2-131">INPUTS</span></span>

### <span data-ttu-id="af0c2-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="af0c2-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="af0c2-133">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="af0c2-133">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="af0c2-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af0c2-134">OUTPUTS</span></span>

### <span data-ttu-id="af0c2-135">Microsoft.Azure.Commands.Batch. Modeller. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="af0c2-135">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="af0c2-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af0c2-136">NOTES</span></span>

## <span data-ttu-id="af0c2-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af0c2-137">RELATED LINKS</span></span>

[<span data-ttu-id="af0c2-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="af0c2-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


