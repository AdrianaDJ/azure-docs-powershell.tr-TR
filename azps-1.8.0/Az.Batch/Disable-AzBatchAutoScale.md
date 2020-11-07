---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: d20a52c3e907bd981bc0a692ebb4aa44495d0960
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761916"
---
# <span data-ttu-id="c3179-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="c3179-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="c3179-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3179-102">SYNOPSIS</span></span>
<span data-ttu-id="c3179-103">Havuz otomatik ölçeklendirmeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="c3179-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="c3179-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3179-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3179-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3179-105">DESCRIPTION</span></span>
<span data-ttu-id="c3179-106">**Disable-Azbatchotomatik ölçeklendirme** cmdlet 'i belirtilen havuzun otomatik ölçeklendirmesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="c3179-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="c3179-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3179-107">EXAMPLES</span></span>

### <span data-ttu-id="c3179-108">Örnek 1: havuz otomatik ölçeklendirmeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="c3179-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="c3179-109">Bu komut MyPool adlı havuz için otomatik ölçeklendirmeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="c3179-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="c3179-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3179-110">PARAMETERS</span></span>

### <span data-ttu-id="c3179-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c3179-111">-BatchContext</span></span>
<span data-ttu-id="c3179-112">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3179-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c3179-113">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c3179-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c3179-114">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="c3179-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c3179-115">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c3179-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c3179-116">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c3179-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c3179-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3179-117">-DefaultProfile</span></span>
<span data-ttu-id="c3179-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3179-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3179-119">-ID</span><span class="sxs-lookup"><span data-stu-id="c3179-119">-Id</span></span>
<span data-ttu-id="c3179-120">Havuzun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3179-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="c3179-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3179-121">CommonParameters</span></span>
<span data-ttu-id="c3179-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3179-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3179-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3179-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3179-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3179-124">INPUTS</span></span>

### <span data-ttu-id="c3179-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c3179-125">System.String</span></span>

### <span data-ttu-id="c3179-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c3179-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c3179-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3179-127">OUTPUTS</span></span>

### <span data-ttu-id="c3179-128">System. void</span><span class="sxs-lookup"><span data-stu-id="c3179-128">System.Void</span></span>

## <span data-ttu-id="c3179-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3179-129">NOTES</span></span>

## <span data-ttu-id="c3179-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3179-130">RELATED LINKS</span></span>

[<span data-ttu-id="c3179-131">Enable-Azbatchotomatik ölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="c3179-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="c3179-132">Test-Azbatchotomatik ölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="c3179-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="c3179-133">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c3179-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

