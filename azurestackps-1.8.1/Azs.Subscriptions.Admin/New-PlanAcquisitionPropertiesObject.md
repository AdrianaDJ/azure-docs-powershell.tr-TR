---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934905"
---
# <span data-ttu-id="47ab8-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="47ab8-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="47ab8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="47ab8-103">Abonelik için eklenti planı alma</span><span class="sxs-lookup"><span data-stu-id="47ab8-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="47ab8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47ab8-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="47ab8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="47ab8-106">Abonelik için eklenti planı alma</span><span class="sxs-lookup"><span data-stu-id="47ab8-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="47ab8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47ab8-107">EXAMPLES</span></span>

### <span data-ttu-id="47ab8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="47ab8-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="47ab8-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="47ab8-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="47ab8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47ab8-110">PARAMETERS</span></span>

### <span data-ttu-id="47ab8-111">-Tanışın kimliği</span><span class="sxs-lookup"><span data-stu-id="47ab8-111">-AcquisitionId</span></span>
<span data-ttu-id="47ab8-112">Alım tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="47ab8-112">Acquisition identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ab8-113">-Tanışanı</span><span class="sxs-lookup"><span data-stu-id="47ab8-113">-AcquisitionTime</span></span>
<span data-ttu-id="47ab8-114">Alım saati.</span><span class="sxs-lookup"><span data-stu-id="47ab8-114">Acquisition time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ab8-115">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="47ab8-115">-ExternalReferenceId</span></span>
<span data-ttu-id="47ab8-116">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="47ab8-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ab8-117">-ID</span><span class="sxs-lookup"><span data-stu-id="47ab8-117">-Id</span></span>
<span data-ttu-id="47ab8-118">Kiracı aboneliği bağlamındaki tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="47ab8-118">Identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ab8-119">-Plankimliği</span><span class="sxs-lookup"><span data-stu-id="47ab8-119">-PlanId</span></span>
<span data-ttu-id="47ab8-120">Kiracı aboneliği bağlamında plan tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="47ab8-120">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ab8-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="47ab8-121">-ProvisioningState</span></span>
<span data-ttu-id="47ab8-122">Sağlama durumu.</span><span class="sxs-lookup"><span data-stu-id="47ab8-122">State of the provisioning.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47ab8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ab8-123">CommonParameters</span></span>
<span data-ttu-id="47ab8-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47ab8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ab8-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ab8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ab8-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47ab8-126">INPUTS</span></span>

## <span data-ttu-id="47ab8-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47ab8-127">OUTPUTS</span></span>

## <span data-ttu-id="47ab8-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47ab8-128">NOTES</span></span>

## <span data-ttu-id="47ab8-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47ab8-129">RELATED LINKS</span></span>

