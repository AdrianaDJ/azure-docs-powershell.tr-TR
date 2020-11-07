---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: cd6181ffb2bba8d71d8a0bf7cbe96d2f8038efc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753362"
---
# <span data-ttu-id="91865-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="91865-101">Get-AzAttestation</span></span>

## <span data-ttu-id="91865-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91865-102">SYNOPSIS</span></span>
<span data-ttu-id="91865-103">Kanıt alır.</span><span class="sxs-lookup"><span data-stu-id="91865-103">Gets an attestation.</span></span>

## <span data-ttu-id="91865-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91865-104">SYNTAX</span></span>

### <span data-ttu-id="91865-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="91865-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91865-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="91865-106">ResourceGroupParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91865-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="91865-107">DESCRIPTION</span></span>
<span data-ttu-id="91865-108">Get-AzAttestation cmdlet 'i bir abonelikteki kanıtlama hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="91865-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="91865-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91865-109">EXAMPLES</span></span>

### <span data-ttu-id="91865-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="91865-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```
<span data-ttu-id="91865-111">"RG1" kaynak grubuna "örnek" ifadesini alma.</span><span class="sxs-lookup"><span data-stu-id="91865-111">Get Attestation "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="91865-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91865-112">PARAMETERS</span></span>

### <span data-ttu-id="91865-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91865-113">-DefaultProfile</span></span>
<span data-ttu-id="91865-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91865-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91865-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="91865-115">-Name</span></span>
<span data-ttu-id="91865-116">Kanıtlama adı.</span><span class="sxs-lookup"><span data-stu-id="91865-116">Attestation Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91865-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91865-117">-ResourceGroupName</span></span>
<span data-ttu-id="91865-118">Sorgulanan kanıtlama ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="91865-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91865-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="91865-119">-ResourceId</span></span>
<span data-ttu-id="91865-120">Sorgulanan kanıtlama ile ilişkili RESOURCEID adını belirtir</span><span class="sxs-lookup"><span data-stu-id="91865-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91865-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91865-121">CommonParameters</span></span>
<span data-ttu-id="91865-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91865-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91865-123">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="91865-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91865-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91865-124">INPUTS</span></span>

### <span data-ttu-id="91865-125">System. String</span><span class="sxs-lookup"><span data-stu-id="91865-125">System.String</span></span>

## <span data-ttu-id="91865-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91865-126">OUTPUTS</span></span>

### <span data-ttu-id="91865-127">Microsoft. Azure. Commands. kanıtlama. modeller. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="91865-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="91865-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91865-128">NOTES</span></span>

## <span data-ttu-id="91865-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91865-129">RELATED LINKS</span></span>
