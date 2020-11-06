---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: e29b5df4a72ff21dbacb0928b298306eb585b493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593593"
---
# <span data-ttu-id="9ac42-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="9ac42-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="9ac42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac42-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac42-103">Toplu iş hesabındaki toplu Iş düğümü Aracısı SKU 'Larını alır.</span><span class="sxs-lookup"><span data-stu-id="9ac42-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ac42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ac42-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ac42-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ac42-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac42-106">**Get-AzureBatchNodeAgentSku** cmdlet 'ı bir Azure toplu hesabında kullanılabilen düğüm Aracısı SKU 'larını alır.</span><span class="sxs-lookup"><span data-stu-id="9ac42-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="9ac42-107">*Batchcontext* parametresini kullanarak hesabı belirtin.</span><span class="sxs-lookup"><span data-stu-id="9ac42-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="9ac42-108">Aramanızı açık bir veri Protokolü (OData) filtresiyle eşleşen STB 'ler olarak daraltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ac42-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="9ac42-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ac42-109">EXAMPLES</span></span>

### <span data-ttu-id="9ac42-110">Örnek 1: tüm kullanılabilir düğüm Aracısı SKU 'Larını alma</span><span class="sxs-lookup"><span data-stu-id="9ac42-110">Example 1: Get all available node agent SKUs</span></span>
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

<span data-ttu-id="9ac42-111">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak aboneliğinizin erişim tuşlarını içeren bir toplu hesap bağlamını alır.</span><span class="sxs-lookup"><span data-stu-id="9ac42-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="9ac42-112">Komut, $Context değişkeninde bağlamı depolar ve sonraki komutta kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9ac42-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="9ac42-113">İkinci komut, toplu Iş desteği olan tüm kullanılabilir düğüm Aracısı SKU 'Larını alır.</span><span class="sxs-lookup"><span data-stu-id="9ac42-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="9ac42-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ac42-114">PARAMETERS</span></span>

### <span data-ttu-id="9ac42-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9ac42-115">-BatchContext</span></span>
<span data-ttu-id="9ac42-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ac42-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9ac42-117">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9ac42-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="9ac42-118">-Filtre</span><span class="sxs-lookup"><span data-stu-id="9ac42-118">-Filter</span></span>
<span data-ttu-id="9ac42-119">Düğüm Aracısı SKU 'Ları için bir OData filtre yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ac42-119">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="9ac42-120">Filtre belirtmezseniz, bu cmdlet toplu Işlemle desteklenen tüm düğüm Aracısı SKU 'Larını döndürür.</span><span class="sxs-lookup"><span data-stu-id="9ac42-120">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="9ac42-121">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9ac42-121">-MaxCount</span></span>
<span data-ttu-id="9ac42-122">Döndürülecek düğüm Aracısı SKU sayısının üst sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ac42-122">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="9ac42-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac42-123">-DefaultProfile</span></span>
<span data-ttu-id="9ac42-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ac42-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ac42-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac42-125">CommonParameters</span></span>
<span data-ttu-id="9ac42-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ac42-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac42-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac42-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac42-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ac42-128">INPUTS</span></span>

### <span data-ttu-id="9ac42-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9ac42-129">BatchAccountContext</span></span>
<span data-ttu-id="9ac42-130">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9ac42-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="9ac42-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ac42-131">OUTPUTS</span></span>

### <span data-ttu-id="9ac42-132">Microsoft.Azure.Commands.Batch. Modeller. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="9ac42-132">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="9ac42-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ac42-133">NOTES</span></span>

## <span data-ttu-id="9ac42-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ac42-134">RELATED LINKS</span></span>

[<span data-ttu-id="9ac42-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9ac42-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


