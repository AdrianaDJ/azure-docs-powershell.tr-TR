---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 124000fdf11b3fa5b90253fc3b9a75c040725ba8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591810"
---
# <span data-ttu-id="fd78e-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="fd78e-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="fd78e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd78e-102">SYNOPSIS</span></span>
<span data-ttu-id="fd78e-103">Havuz otomatik ölçeklendirmeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fd78e-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd78e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd78e-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd78e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd78e-105">DESCRIPTION</span></span>
<span data-ttu-id="fd78e-106">**Disable-AzureBatchAutoScale** cmdlet 'i belirtilen havuzun otomatik ölçeklendirmesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fd78e-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="fd78e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd78e-107">EXAMPLES</span></span>

### <span data-ttu-id="fd78e-108">Örnek 1: havuz otomatik ölçeklendirmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="fd78e-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="fd78e-109">Bu komut MyPool adlı havuz için otomatik ölçeklendirmeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="fd78e-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="fd78e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd78e-110">PARAMETERS</span></span>

### <span data-ttu-id="fd78e-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fd78e-111">-BatchContext</span></span>
<span data-ttu-id="fd78e-112">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd78e-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fd78e-113">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fd78e-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="fd78e-114">-ID</span><span class="sxs-lookup"><span data-stu-id="fd78e-114">-Id</span></span>
<span data-ttu-id="fd78e-115">Havuzun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd78e-115">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="fd78e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd78e-116">-DefaultProfile</span></span>
<span data-ttu-id="fd78e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd78e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd78e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd78e-118">CommonParameters</span></span>
<span data-ttu-id="fd78e-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd78e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd78e-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd78e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd78e-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd78e-121">INPUTS</span></span>

### <span data-ttu-id="fd78e-122">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fd78e-122">BatchAccountContext</span></span>
<span data-ttu-id="fd78e-123">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fd78e-123">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="fd78e-124">Dizisi</span><span class="sxs-lookup"><span data-stu-id="fd78e-124">String</span></span>
<span data-ttu-id="fd78e-125">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fd78e-125">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="fd78e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd78e-126">OUTPUTS</span></span>

## <span data-ttu-id="fd78e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd78e-127">NOTES</span></span>

## <span data-ttu-id="fd78e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd78e-128">RELATED LINKS</span></span>

[<span data-ttu-id="fd78e-129">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="fd78e-129">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="fd78e-130">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="fd78e-130">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="fd78e-131">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="fd78e-131">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


