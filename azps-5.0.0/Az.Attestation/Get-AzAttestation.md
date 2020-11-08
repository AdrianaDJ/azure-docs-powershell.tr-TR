---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276141"
---
# <span data-ttu-id="f2dbe-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="f2dbe-101">Get-AzAttestation</span></span>

## <span data-ttu-id="f2dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="f2dbe-103">Kanıt alır.</span><span class="sxs-lookup"><span data-stu-id="f2dbe-103">Gets an attestation.</span></span>

## <span data-ttu-id="f2dbe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2dbe-104">SYNTAX</span></span>

### <span data-ttu-id="f2dbe-105">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2dbe-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2dbe-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f2dbe-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2dbe-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2dbe-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2dbe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2dbe-108">DESCRIPTION</span></span>
<span data-ttu-id="f2dbe-109">Get-AzAttestation cmdlet 'i bir abonelikteki kanıtlama hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="f2dbe-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="f2dbe-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2dbe-110">EXAMPLES</span></span>

### <span data-ttu-id="f2dbe-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f2dbe-111">Example 1</span></span>
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

<span data-ttu-id="f2dbe-112">Kaynak Grup *PSH-test-RG* Için kanıt sağlayıcı *pshtest* alın.</span><span class="sxs-lookup"><span data-stu-id="f2dbe-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="f2dbe-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f2dbe-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/sharedcus
Location          : Central US
ResourceGroupName :
Name              : sharedcus
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedcus.cus.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/shareduks
Location          : UK South
ResourceGroupName :
Name              : shareduks
Status            : Ready
TrustModel        : AAD
AttestUri         : https://shareduks.uks.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="f2dbe-114">Kullanılabilir tüm kanıtlama varsayılan sağlayıcılarını edinin</span><span class="sxs-lookup"><span data-stu-id="f2dbe-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="f2dbe-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="f2dbe-115">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider -Location "East US 2"
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="f2dbe-116">*Doğu US 2* konumundan kanıt varsayılan sağlayıcısını al</span><span class="sxs-lookup"><span data-stu-id="f2dbe-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="f2dbe-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2dbe-117">PARAMETERS</span></span>

### <span data-ttu-id="f2dbe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2dbe-118">-DefaultProfile</span></span>
<span data-ttu-id="f2dbe-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2dbe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2dbe-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="f2dbe-120">-DefaultProvider</span></span>
<span data-ttu-id="f2dbe-121">Bu, varsayılan kanıtlama sağlayıcısı isteğinin olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2dbe-121">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2dbe-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="f2dbe-122">-Location</span></span>
<span data-ttu-id="f2dbe-123">Varsayılan kanıtlama sağlayıcısının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2dbe-123">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2dbe-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f2dbe-124">-Name</span></span>
<span data-ttu-id="f2dbe-125">Kanıtlama adı.</span><span class="sxs-lookup"><span data-stu-id="f2dbe-125">Attestation Name.</span></span>

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

### <span data-ttu-id="f2dbe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2dbe-126">-ResourceGroupName</span></span>
<span data-ttu-id="f2dbe-127">Sorgulanan kanıtlama ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f2dbe-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="f2dbe-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f2dbe-128">-ResourceId</span></span>
<span data-ttu-id="f2dbe-129">Sorgulanan kanıtlama ile ilişkili RESOURCEID adını belirtir</span><span class="sxs-lookup"><span data-stu-id="f2dbe-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="f2dbe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2dbe-130">CommonParameters</span></span>
<span data-ttu-id="f2dbe-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2dbe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2dbe-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f2dbe-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2dbe-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2dbe-133">INPUTS</span></span>

### <span data-ttu-id="f2dbe-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f2dbe-134">System.String</span></span>

## <span data-ttu-id="f2dbe-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2dbe-135">OUTPUTS</span></span>

### <span data-ttu-id="f2dbe-136">Microsoft. Azure. Commands. kanıtlama. modeller. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="f2dbe-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="f2dbe-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2dbe-137">NOTES</span></span>

## <span data-ttu-id="f2dbe-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2dbe-138">RELATED LINKS</span></span>
