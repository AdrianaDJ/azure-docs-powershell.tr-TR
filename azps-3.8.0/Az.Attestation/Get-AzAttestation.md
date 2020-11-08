---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: a18222c40dc5c56bd2d67afb8d0df35b7aedc532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098218"
---
# <span data-ttu-id="0f099-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="0f099-101">Get-AzAttestation</span></span>

## <span data-ttu-id="0f099-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f099-102">SYNOPSIS</span></span>
<span data-ttu-id="0f099-103">Kanıt alır.</span><span class="sxs-lookup"><span data-stu-id="0f099-103">Gets an attestation.</span></span>

## <span data-ttu-id="0f099-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f099-104">SYNTAX</span></span>

### <span data-ttu-id="0f099-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0f099-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f099-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0f099-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f099-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f099-107">DESCRIPTION</span></span>
<span data-ttu-id="0f099-108">Get-AzAttestation cmdlet 'i bir abonelikteki kanıtlama hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0f099-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="0f099-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f099-109">EXAMPLES</span></span>

### <span data-ttu-id="0f099-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0f099-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                                       
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest.us.attest.azure.net
Tags              : {Production, Example}
TagsTable         :
                    Name        Value
                    ==========  =====
                    Production  False
                    Example     True
```

<span data-ttu-id="0f099-111">Kaynak Grup *PSH-test-RG* Için kanıt sağlayıcı *pshtest* alın.</span><span class="sxs-lookup"><span data-stu-id="0f099-111">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

## <span data-ttu-id="0f099-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f099-112">PARAMETERS</span></span>

### <span data-ttu-id="0f099-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f099-113">-DefaultProfile</span></span>
<span data-ttu-id="0f099-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f099-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f099-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f099-115">-Name</span></span>
<span data-ttu-id="0f099-116">Kanıtlama adı.</span><span class="sxs-lookup"><span data-stu-id="0f099-116">Attestation Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f099-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f099-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f099-118">Sorgulanan kanıtlama ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f099-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f099-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0f099-119">-ResourceId</span></span>
<span data-ttu-id="0f099-120">Sorgulanan kanıtlama ile ilişkili RESOURCEID adını belirtir</span><span class="sxs-lookup"><span data-stu-id="0f099-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f099-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f099-121">CommonParameters</span></span>
<span data-ttu-id="0f099-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f099-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f099-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0f099-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f099-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f099-124">INPUTS</span></span>

### <span data-ttu-id="0f099-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0f099-125">System.String</span></span>

## <span data-ttu-id="0f099-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f099-126">OUTPUTS</span></span>

### <span data-ttu-id="0f099-127">Microsoft. Azure. Commands. kanıtlama. modeller. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="0f099-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="0f099-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f099-128">NOTES</span></span>

## <span data-ttu-id="0f099-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f099-129">RELATED LINKS</span></span>
