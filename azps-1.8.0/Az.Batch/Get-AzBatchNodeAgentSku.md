---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
ms.openlocfilehash: 8f7228a540456e76e4f7a22d70d00969a9ef568c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761884"
---
# <span data-ttu-id="e2e5f-101">Get-AzBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="e2e5f-101">Get-AzBatchNodeAgentSku</span></span>

## <span data-ttu-id="e2e5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e5f-103">Toplu iş hesabındaki toplu Iş düğümü Aracısı SKU 'Larını alır.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

## <span data-ttu-id="e2e5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2e5f-104">SYNTAX</span></span>

```
Get-AzBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2e5f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2e5f-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e5f-106">**Get-AzBatchNodeAgentSku** cmdlet 'i, bir Azure toplu hesabında kullanılabilen düğüm Aracısı SKU 'larını alır.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-106">The **Get-AzBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="e2e5f-107">*Batchcontext* parametresini kullanarak hesabı belirtin.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="e2e5f-108">Aramanızı açık bir veri Protokolü (OData) filtresiyle eşleşen STB 'ler olarak daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="e2e5f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2e5f-109">EXAMPLES</span></span>

### <span data-ttu-id="e2e5f-110">Örnek 1: tüm kullanılabilir düğüm Aracısı SKU 'Larını alma</span><span class="sxs-lookup"><span data-stu-id="e2e5f-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="e2e5f-111">İlk komut, **Get-AzBatchAccountKeys** kullanarak aboneliğinizin erişim tuşlarını içeren bir toplu hesap bağlamı alır.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="e2e5f-112">Komut, $Context değişkeninde bağlamı depolar ve sonraki komutta kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="e2e5f-113">İkinci komut, toplu Iş desteği olan tüm kullanılabilir düğüm Aracısı SKU 'Larını alır.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="e2e5f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2e5f-114">PARAMETERS</span></span>

### <span data-ttu-id="e2e5f-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e2e5f-115">-BatchContext</span></span>
<span data-ttu-id="e2e5f-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e2e5f-117">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e2e5f-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e2e5f-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e2e5f-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e2e5f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e5f-121">-DefaultProfile</span></span>
<span data-ttu-id="e2e5f-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2e5f-123">-Filtre</span><span class="sxs-lookup"><span data-stu-id="e2e5f-123">-Filter</span></span>
<span data-ttu-id="e2e5f-124">Düğüm Aracısı SKU 'Ları için bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="e2e5f-125">Filtre belirtmezseniz, bu cmdlet toplu Işlemle desteklenen tüm düğüm Aracısı SKU 'Larını döndürür.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="e2e5f-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e2e5f-126">-MaxCount</span></span>
<span data-ttu-id="e2e5f-127">Döndürülecek düğüm Aracısı SKU sayısının üst sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-127">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="e2e5f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e5f-128">CommonParameters</span></span>
<span data-ttu-id="e2e5f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2e5f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e5f-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e5f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e5f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2e5f-131">INPUTS</span></span>

### <span data-ttu-id="e2e5f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e2e5f-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e2e5f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2e5f-133">OUTPUTS</span></span>

### <span data-ttu-id="e2e5f-134">Microsoft.Azure.Commands.Batch. Modeller. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="e2e5f-134">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="e2e5f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2e5f-135">NOTES</span></span>

## <span data-ttu-id="e2e5f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2e5f-136">RELATED LINKS</span></span>

[<span data-ttu-id="e2e5f-137">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="e2e5f-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


