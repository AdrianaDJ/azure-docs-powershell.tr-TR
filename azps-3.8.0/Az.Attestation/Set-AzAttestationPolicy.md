---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098203"
---
# <span data-ttu-id="06526-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="06526-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="06526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06526-102">SYNOPSIS</span></span>
<span data-ttu-id="06526-103">Azure Attestationn 'de ilkeyi bir kiracıdan ayarlar.</span><span class="sxs-lookup"><span data-stu-id="06526-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="06526-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06526-104">SYNTAX</span></span>

### <span data-ttu-id="06526-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="06526-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06526-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="06526-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06526-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="06526-107">DESCRIPTION</span></span>
<span data-ttu-id="06526-108">Set-AzAttestationPolicy cmdlet 'i Azure kanıt 'nda ilkeyi bir kiracı 'dan ayarlar.</span><span class="sxs-lookup"><span data-stu-id="06526-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="06526-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06526-109">EXAMPLES</span></span>

### <span data-ttu-id="06526-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="06526-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="06526-111">Metin ilkesi biçimi (varsayılan) kullanarak kanıt sağlayıcısı *pshtest* için t türü *SgxEnclave* için Kullanıcı tanımlı ilke 'yi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="06526-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="06526-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="06526-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="06526-113">JWT ilke biçimini kullanarak kanıtlama sağlayıcısı *pshtest* için t türü *SgxEnclave* için Kullanıcı tanımlı ilke 'yi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="06526-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="06526-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06526-114">PARAMETERS</span></span>

### <span data-ttu-id="06526-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06526-115">-DefaultProfile</span></span>
<span data-ttu-id="06526-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06526-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06526-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="06526-117">-Name</span></span>
<span data-ttu-id="06526-118">Kiracının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06526-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="06526-119">Bu cmdlet, bu parametrenin belirttiği kiracı için kanıtlama ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="06526-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="06526-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="06526-120">-PassThru</span></span>
<span data-ttu-id="06526-121">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="06526-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="06526-122">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="06526-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="06526-123">-İlke</span><span class="sxs-lookup"><span data-stu-id="06526-123">-Policy</span></span>
<span data-ttu-id="06526-124">Ayarlanacak ilke belgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06526-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="06526-125">İlke biçimi, metin veya JSON Web belirteci (JWT) olabilir.</span><span class="sxs-lookup"><span data-stu-id="06526-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="06526-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="06526-126">-PolicyFormat</span></span>
<span data-ttu-id="06526-127">İlkenin biçimini (metin veya JWT) belirtir.</span><span class="sxs-lookup"><span data-stu-id="06526-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="06526-128">Varsayılan ilke biçimi metindir.</span><span class="sxs-lookup"><span data-stu-id="06526-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="06526-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06526-129">-ResourceGroupName</span></span>
<span data-ttu-id="06526-130">Bir kanıt sağlayıcısının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06526-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="06526-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="06526-131">-ResourceId</span></span>
<span data-ttu-id="06526-132">Bir kanıt sağlayıcısının RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="06526-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="06526-133">-T</span><span class="sxs-lookup"><span data-stu-id="06526-133">-Tee</span></span>
<span data-ttu-id="06526-134">Güvenilir yürütme ortamının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="06526-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="06526-135">Dört tür ortam desteklenir: SgxEnclave, Openenclaand, CyResComponent ve Vbsenclaand.</span><span class="sxs-lookup"><span data-stu-id="06526-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="06526-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="06526-136">-Confirm</span></span>
<span data-ttu-id="06526-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="06526-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06526-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06526-138">-WhatIf</span></span>
<span data-ttu-id="06526-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06526-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06526-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="06526-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06526-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06526-141">CommonParameters</span></span>
<span data-ttu-id="06526-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06526-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06526-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="06526-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06526-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06526-144">INPUTS</span></span>

### <span data-ttu-id="06526-145">System. String</span><span class="sxs-lookup"><span data-stu-id="06526-145">System.String</span></span>

## <span data-ttu-id="06526-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06526-146">OUTPUTS</span></span>

### <span data-ttu-id="06526-147">System. String</span><span class="sxs-lookup"><span data-stu-id="06526-147">System.String</span></span>

## <span data-ttu-id="06526-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06526-148">NOTES</span></span>

## <span data-ttu-id="06526-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06526-149">RELATED LINKS</span></span>
