---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: ce21b116ceb41bfdfb26008dd44c914f3198ab39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753361"
---
# <span data-ttu-id="8819b-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="8819b-101">New-AzAttestation</span></span>

## <span data-ttu-id="8819b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8819b-102">SYNOPSIS</span></span>
<span data-ttu-id="8819b-103">Kanıt oluşturur</span><span class="sxs-lookup"><span data-stu-id="8819b-103">Creates an attestation</span></span>

## <span data-ttu-id="8819b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8819b-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> [-AttestationPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8819b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8819b-105">DESCRIPTION</span></span>
<span data-ttu-id="8819b-106">New-AzAttestation cmdlet 'i belirtilen kaynak grubunda bir kanıt oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8819b-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="8819b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8819b-107">EXAMPLES</span></span>

### <span data-ttu-id="8819b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8819b-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```

<span data-ttu-id="8819b-109">Geçerli abonelikte yeni bir kanıt "örnek" oluşturun, kaynak grubu "RG1"</span><span class="sxs-lookup"><span data-stu-id="8819b-109">Create a new Attestation "example" in current Subscription, Resource Group "rg1"</span></span>

## <span data-ttu-id="8819b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8819b-110">PARAMETERS</span></span>

### <span data-ttu-id="8819b-111">-AttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="8819b-111">-AttestationPolicy</span></span>
<span data-ttu-id="8819b-112">Kanıtlama oluşturulacak kanıtlama ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8819b-112">Specifies the attestation policy passed in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8819b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8819b-113">-DefaultProfile</span></span>
<span data-ttu-id="8819b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8819b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8819b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="8819b-115">-Name</span></span>
<span data-ttu-id="8819b-116">Oluşturulacak örnek adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8819b-116">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="8819b-117">Ad, harf, sayı veya kısa çizgi bileşimleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="8819b-117">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="8819b-118">Ad bir harfle veya rakamla başlamalıdır ve bitmelidir.</span><span class="sxs-lookup"><span data-stu-id="8819b-118">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="8819b-119">Ad, evrensel olarak benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8819b-119">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8819b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8819b-120">-ResourceGroupName</span></span>
<span data-ttu-id="8819b-121">Kanıtlamayı oluşturacağınız varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8819b-121">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8819b-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="8819b-122">-Confirm</span></span>
<span data-ttu-id="8819b-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8819b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8819b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8819b-124">-WhatIf</span></span>
<span data-ttu-id="8819b-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8819b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8819b-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8819b-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8819b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8819b-127">CommonParameters</span></span>
<span data-ttu-id="8819b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8819b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8819b-129">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8819b-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8819b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8819b-130">INPUTS</span></span>

### <span data-ttu-id="8819b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8819b-131">System.String</span></span>

## <span data-ttu-id="8819b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8819b-132">OUTPUTS</span></span>

### <span data-ttu-id="8819b-133">Microsoft. Azure. Commands. kanıtlama. modeller. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="8819b-133">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="8819b-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8819b-134">NOTES</span></span>

## <span data-ttu-id="8819b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8819b-135">RELATED LINKS</span></span>
