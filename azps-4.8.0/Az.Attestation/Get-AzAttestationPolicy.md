---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 64a74902d1a5b10ed36c635b58910246634e68b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108524"
---
# <span data-ttu-id="f218e-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="f218e-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="f218e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f218e-102">SYNOPSIS</span></span>
<span data-ttu-id="f218e-103">Azure kanıtlama 'ndaki bir kiracıdan ilkeyi alır.</span><span class="sxs-lookup"><span data-stu-id="f218e-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f218e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f218e-104">SYNTAX</span></span>

### <span data-ttu-id="f218e-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f218e-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f218e-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f218e-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f218e-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="f218e-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestationPolicy [-Location] <String> [-DefaultProvider] -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f218e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f218e-108">DESCRIPTION</span></span>
<span data-ttu-id="f218e-109">Get-AzAttestationPolicy cmdlet 'i Azure kanıtlama 'ndaki bir kiracıdan ilkeyi alır.</span><span class="sxs-lookup"><span data-stu-id="f218e-109">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f218e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f218e-110">EXAMPLES</span></span>

### <span data-ttu-id="f218e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f218e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave                                                                                                                                                                                                                    
Text       : version= 1.0;
             authorizationrules{
                 c:[type=="$is-debuggable"] => permit();
             };
             issuancerules{
                 c:[type=="$is-debuggable"] => issue(type="is-debuggable", value=c.value);
                 c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);
                 c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave", value=c.value);
                 c:[type=="$product-id"] => issue(type="product-id", value=c.value);
                 c:[type=="$svn"] => issue(type="svn", value=c.value);
                 c:[type=="$tee"] => issue(type="tee", value=c.value);
                 c:[type=="$tee-future"] => issue(type="tee-future", value=c.value);
             };

TextLength : 604
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3T3cwS1lYVjBhRzl5YVhwaGRHbHZibkoxYkdWemV3MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2FYTXRaR1ZpZFdkbllXSnNaU0pkSUQwLUlIQmxjbTFwZENncE93MEtmVHNOQ21semMzVmhibU5sY25Wc1pYTjdEUW9nSUNBZ1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2MyZDRMVzF5YzJsbmJtVnlJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGljMmQ0TFcxeWMybG5ibVZ5SWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVJ6WjNndGJYSmxibU5zWVhabElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWMyZDRMVzF5Wlc1amJHRjJaU0lzSUhaaGJIVmxQV011ZG1Gc2RXVXBPdzBLSUNBZ0lHTTZXM1I1Y0dVOVBTSWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHNOQ2lBZ0lDQmpPbHQwZVhCbFBUMGlKSE4yYmlKZElEMC1JR2x6YzNWbEtIUjVjR1U5SW5OMmJpSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2RHVmxJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGlkR1ZsSWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVIwWldVdFpuVjBkWEpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpZEdWbExXWjFkSFZ5WlNJc0lIWmhiSFZsUFdNdWRtRnNkV1VwT3cwS2ZUc05DZyJ9.
JwtLength  : 1129
Algorithm  : none
```

<span data-ttu-id="f218e-112">T türü *SgxEnclave* Için kanıtlama sağlayıcı *pshtest* ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="f218e-112">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="f218e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f218e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -DefaultProvider -Location "UK South" -Tee SgxEnclave
Text       : version= 1.0;authorizationrules{c:[type=="$is-debuggable"] => permit();};issuancerules{c:[type=="$is-debuggable"] => issue(type="is-debuggable",
             value=c.value);c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave",
             value=c.value);c:[type=="$product-id"] => issue(type="product-id", value=c.value);c:[type=="$svn"] => issue(type="svn", value=c.value);c:[type=="$tee"]
             => issue(type="tee", value=c.value);};
TextLength : 479
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3TzJGMWRHaHZjbWw2WVhScGIyNXlkV3hsYzN0ak9sdDBlWEJsUFQwaUpHbHpMV1JsWW5WbloyRmliR1Vp
             WFNBOVBpQndaWEp0YVhRb0tUdDlPMmx6YzNWaGJtTmxjblZzWlhON1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pT
             SXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBTSWtjMmQ0TFcxeWMybG5ibVZ5SWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXljMmxuYm1WeUlpd2dkbUZzZFdVOVl5NTJZV3gx
             WlNrN1l6cGJkSGx3WlQwOUlpUnpaM2d0YlhKbGJtTnNZWFpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXlaVzVqYkdGMlpTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBT
             SWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHRqT2x0MGVYQmxQVDBpSkhOMmJpSmRJRDAtSUdsemMzVmxLSFI1
             Y0dVOUluTjJiaUlzSUhaaGJIVmxQV011ZG1Gc2RXVXBPMk02VzNSNWNHVTlQU0lrZEdWbElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWRHVmxJaXdnZG1Gc2RXVTlZeTUyWVd4MVpTazdmVHMifQ.
JwtLength  : 907
Algorithm  : none
```

<span data-ttu-id="f218e-114">En fazla% t tür *SgxEnclave* Için, *İngiltere* varsayılan sağlayıcısının ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="f218e-114">Gets the policy for Attestation Default Provider from Location *UK South* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="f218e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f218e-115">PARAMETERS</span></span>

### <span data-ttu-id="f218e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f218e-116">-DefaultProfile</span></span>
<span data-ttu-id="f218e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f218e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f218e-118">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="f218e-118">-DefaultProvider</span></span>
<span data-ttu-id="f218e-119">Bu, varsayılan kanıtlama sağlayıcısı isteğinin olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f218e-119">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f218e-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="f218e-120">-Location</span></span>
<span data-ttu-id="f218e-121">Varsayılan kanıtlama sağlayıcısının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f218e-121">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f218e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f218e-122">-Name</span></span>
<span data-ttu-id="f218e-123">Kiracının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f218e-123">Specifies a name of the tenant.</span></span>
<span data-ttu-id="f218e-124">Bu cmdlet, bu parametrenin belirttiği kiracı için kanıtlama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="f218e-124">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="f218e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f218e-125">-ResourceGroupName</span></span>
<span data-ttu-id="f218e-126">Bir kanıt sağlayıcısının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f218e-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="f218e-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f218e-127">-ResourceId</span></span>
<span data-ttu-id="f218e-128">Bir kanıt sağlayıcısının RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f218e-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="f218e-129">-T</span><span class="sxs-lookup"><span data-stu-id="f218e-129">-Tee</span></span>
<span data-ttu-id="f218e-130">Güvenilir yürütme ortamının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f218e-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="f218e-131">Dört tür ortamı destekliyoruz: SgxEnclave, Openenclaand, CyResComponent ve Vbsenclade.</span><span class="sxs-lookup"><span data-stu-id="f218e-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="f218e-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="f218e-132">-Confirm</span></span>
<span data-ttu-id="f218e-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f218e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f218e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f218e-134">-WhatIf</span></span>
<span data-ttu-id="f218e-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f218e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f218e-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f218e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f218e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f218e-137">CommonParameters</span></span>
<span data-ttu-id="f218e-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f218e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f218e-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f218e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f218e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f218e-140">INPUTS</span></span>

### <span data-ttu-id="f218e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f218e-141">System.String</span></span>

## <span data-ttu-id="f218e-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f218e-142">OUTPUTS</span></span>

### <span data-ttu-id="f218e-143">Microsoft. Azure. Commands. kanıtlama. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f218e-143">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="f218e-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f218e-144">NOTES</span></span>

## <span data-ttu-id="f218e-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f218e-145">RELATED LINKS</span></span>
