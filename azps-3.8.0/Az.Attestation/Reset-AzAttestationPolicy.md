---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: a2b8d83254c84ee974173611912dd9b21cb7a26d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098204"
---
# <span data-ttu-id="bfd47-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="bfd47-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="bfd47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfd47-102">SYNOPSIS</span></span>
<span data-ttu-id="bfd47-103">İlkeyi Azure Attestationn 'de bir kiracıdan sıfırlar.}</span><span class="sxs-lookup"><span data-stu-id="bfd47-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="bfd47-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfd47-104">SYNTAX</span></span>

### <span data-ttu-id="bfd47-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfd47-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfd47-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bfd47-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfd47-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfd47-107">DESCRIPTION</span></span>
<span data-ttu-id="bfd47-108">Reset-AzAttestationPolicy cmdlet 'i, Azure kanıt 'nda Kullanıcı tanımlı kanıtlama ilkesini bir kiracıdan sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="bfd47-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="bfd47-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfd47-109">EXAMPLES</span></span>

### <span data-ttu-id="bfd47-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bfd47-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="bfd47-111">Kuralı kanıt türü *SgxEnclave* *için kanıtlama sağlayıcısı için* varsayılan olarak sıfırlayın.</span><span class="sxs-lookup"><span data-stu-id="bfd47-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="bfd47-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfd47-112">PARAMETERS</span></span>

### <span data-ttu-id="bfd47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfd47-113">-DefaultProfile</span></span>
<span data-ttu-id="bfd47-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bfd47-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfd47-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="bfd47-115">-Name</span></span>
<span data-ttu-id="bfd47-116">Kiracının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfd47-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="bfd47-117">Bu cmdlet, bu parametrenin belirttiği kiracı için kanıtlama ilkesini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="bfd47-117">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfd47-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bfd47-118">-PassThru</span></span>
<span data-ttu-id="bfd47-119">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="bfd47-119">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="bfd47-120">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="bfd47-120">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfd47-121">-İlke</span><span class="sxs-lookup"><span data-stu-id="bfd47-121">-Policy</span></span>
<span data-ttu-id="bfd47-122">Sıfırlanacak ilke belgesini açıklayan JSON Web belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfd47-122">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="bfd47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfd47-123">-ResourceGroupName</span></span>
<span data-ttu-id="bfd47-124">Bir kanıt sağlayıcısının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfd47-124">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfd47-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bfd47-125">-ResourceId</span></span>
<span data-ttu-id="bfd47-126">Bir kanıt sağlayıcısının RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfd47-126">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="bfd47-127">-T</span><span class="sxs-lookup"><span data-stu-id="bfd47-127">-Tee</span></span>
<span data-ttu-id="bfd47-128">Güvenilir yürütme ortamının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bfd47-128">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="bfd47-129">Dört tür ortamı destekliyoruz: SgxEnclave, Openenclaand, CyResComponent ve Vbsenclade.</span><span class="sxs-lookup"><span data-stu-id="bfd47-129">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfd47-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="bfd47-130">-Confirm</span></span>
<span data-ttu-id="bfd47-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bfd47-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfd47-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfd47-132">-WhatIf</span></span>
<span data-ttu-id="bfd47-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bfd47-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfd47-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bfd47-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfd47-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfd47-135">CommonParameters</span></span>
<span data-ttu-id="bfd47-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfd47-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfd47-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bfd47-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfd47-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfd47-138">INPUTS</span></span>

### <span data-ttu-id="bfd47-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bfd47-139">System.String</span></span>

## <span data-ttu-id="bfd47-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfd47-140">OUTPUTS</span></span>

### <span data-ttu-id="bfd47-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bfd47-141">System.Boolean</span></span>

## <span data-ttu-id="bfd47-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfd47-142">NOTES</span></span>

## <span data-ttu-id="bfd47-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfd47-143">RELATED LINKS</span></span>
