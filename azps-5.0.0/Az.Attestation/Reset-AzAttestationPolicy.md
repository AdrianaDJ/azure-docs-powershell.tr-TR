---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321893"
---
# <span data-ttu-id="14f22-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="14f22-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="14f22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14f22-102">SYNOPSIS</span></span>
<span data-ttu-id="14f22-103">İlkeyi Azure Attestationn 'de bir kiracıdan sıfırlar.}</span><span class="sxs-lookup"><span data-stu-id="14f22-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="14f22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14f22-104">SYNTAX</span></span>

### <span data-ttu-id="14f22-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14f22-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14f22-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="14f22-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14f22-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="14f22-107">DESCRIPTION</span></span>
<span data-ttu-id="14f22-108">Reset-AzAttestationPolicy cmdlet 'i, Azure kanıt 'nda Kullanıcı tanımlı kanıtlama ilkesini bir kiracıdan sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="14f22-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="14f22-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14f22-109">EXAMPLES</span></span>

### <span data-ttu-id="14f22-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="14f22-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="14f22-111">Kuralı kanıt türü *SgxEnclave* *için kanıtlama sağlayıcısı için* varsayılan olarak sıfırlayın.</span><span class="sxs-lookup"><span data-stu-id="14f22-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="14f22-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="14f22-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="14f22-113">Kanıtlama sağlayıcısı *pshtest* yalıtılmış güven modelini kullanacak şekilde yapılandırıldıysa, imzasız bir ilke ekleyerek Ilkeyi, t türü *SgxEnclave* için varsayılan değere sıfırlayın.</span><span class="sxs-lookup"><span data-stu-id="14f22-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="14f22-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14f22-114">PARAMETERS</span></span>

### <span data-ttu-id="14f22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f22-115">-DefaultProfile</span></span>
<span data-ttu-id="14f22-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14f22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14f22-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="14f22-117">-Name</span></span>
<span data-ttu-id="14f22-118">Kiracının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14f22-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="14f22-119">Bu cmdlet, bu parametrenin belirttiği kiracı için kanıtlama ilkesini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="14f22-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="14f22-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="14f22-120">-PassThru</span></span>
<span data-ttu-id="14f22-121">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="14f22-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="14f22-122">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="14f22-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="14f22-123">-İlke</span><span class="sxs-lookup"><span data-stu-id="14f22-123">-Policy</span></span>
<span data-ttu-id="14f22-124">Sıfırlanacak ilke belgesini açıklayan JSON Web belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="14f22-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="14f22-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14f22-125">-ResourceGroupName</span></span>
<span data-ttu-id="14f22-126">Bir kanıt sağlayıcısının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="14f22-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="14f22-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="14f22-127">-ResourceId</span></span>
<span data-ttu-id="14f22-128">Bir kanıt sağlayıcısının RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="14f22-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="14f22-129">-T</span><span class="sxs-lookup"><span data-stu-id="14f22-129">-Tee</span></span>
<span data-ttu-id="14f22-130">Güvenilir yürütme ortamının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="14f22-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="14f22-131">Dört tür ortamı destekliyoruz: SgxEnclave, Openenclaand, CyResComponent ve Vbsenclade.</span><span class="sxs-lookup"><span data-stu-id="14f22-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="14f22-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="14f22-132">-Confirm</span></span>
<span data-ttu-id="14f22-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="14f22-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14f22-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14f22-134">-WhatIf</span></span>
<span data-ttu-id="14f22-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="14f22-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14f22-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="14f22-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14f22-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f22-137">CommonParameters</span></span>
<span data-ttu-id="14f22-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14f22-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f22-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="14f22-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f22-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14f22-140">INPUTS</span></span>

### <span data-ttu-id="14f22-141">System. String</span><span class="sxs-lookup"><span data-stu-id="14f22-141">System.String</span></span>

## <span data-ttu-id="14f22-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14f22-142">OUTPUTS</span></span>

### <span data-ttu-id="14f22-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="14f22-143">System.Boolean</span></span>

## <span data-ttu-id="14f22-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14f22-144">NOTES</span></span>

## <span data-ttu-id="14f22-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14f22-145">RELATED LINKS</span></span>
