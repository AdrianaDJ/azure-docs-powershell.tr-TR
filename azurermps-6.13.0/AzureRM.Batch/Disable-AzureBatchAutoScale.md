---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 403e38ae72f927b4b98107161b62859aa57bacf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762320"
---
# <span data-ttu-id="369a7-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="369a7-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="369a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="369a7-102">SYNOPSIS</span></span>
<span data-ttu-id="369a7-103">Havuz otomatik ölçeklendirmeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="369a7-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="369a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="369a7-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="369a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="369a7-105">DESCRIPTION</span></span>
<span data-ttu-id="369a7-106">**Disable-AzureBatchAutoScale** cmdlet 'i belirtilen havuzun otomatik ölçeklendirmesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="369a7-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="369a7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="369a7-107">EXAMPLES</span></span>

### <span data-ttu-id="369a7-108">Örnek 1: havuz otomatik ölçeklendirmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="369a7-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="369a7-109">Bu komut MyPool adlı havuz için otomatik ölçeklendirmeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="369a7-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="369a7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="369a7-110">PARAMETERS</span></span>

### <span data-ttu-id="369a7-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="369a7-111">-BatchContext</span></span>
<span data-ttu-id="369a7-112">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="369a7-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="369a7-113">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="369a7-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="369a7-114">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="369a7-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="369a7-115">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="369a7-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="369a7-116">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="369a7-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="369a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="369a7-117">-DefaultProfile</span></span>
<span data-ttu-id="369a7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="369a7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="369a7-119">-ID</span><span class="sxs-lookup"><span data-stu-id="369a7-119">-Id</span></span>
<span data-ttu-id="369a7-120">Havuzun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="369a7-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="369a7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="369a7-121">CommonParameters</span></span>
<span data-ttu-id="369a7-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="369a7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="369a7-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="369a7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="369a7-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="369a7-124">INPUTS</span></span>

### <span data-ttu-id="369a7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="369a7-125">System.String</span></span>

### <span data-ttu-id="369a7-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="369a7-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="369a7-127">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="369a7-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="369a7-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="369a7-128">OUTPUTS</span></span>

### <span data-ttu-id="369a7-129">System. void</span><span class="sxs-lookup"><span data-stu-id="369a7-129">System.Void</span></span>

## <span data-ttu-id="369a7-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="369a7-130">NOTES</span></span>

## <span data-ttu-id="369a7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="369a7-131">RELATED LINKS</span></span>

[<span data-ttu-id="369a7-132">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="369a7-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="369a7-133">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="369a7-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="369a7-134">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="369a7-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

