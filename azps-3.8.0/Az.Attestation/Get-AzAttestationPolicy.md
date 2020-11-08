---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 0c36f5fb87e3d247a48031bdc735c077a577ac27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098213"
---
# <span data-ttu-id="f03d8-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="f03d8-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="f03d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f03d8-102">SYNOPSIS</span></span>
<span data-ttu-id="f03d8-103">Azure kanıtlama 'ndaki bir kiracıdan ilkeyi alır.</span><span class="sxs-lookup"><span data-stu-id="f03d8-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f03d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f03d8-104">SYNTAX</span></span>

### <span data-ttu-id="f03d8-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f03d8-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f03d8-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f03d8-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f03d8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f03d8-107">DESCRIPTION</span></span>
<span data-ttu-id="f03d8-108">Get-AzAttestationPolicy cmdlet 'i Azure kanıtlama 'ndaki bir kiracıdan ilkeyi alır.</span><span class="sxs-lookup"><span data-stu-id="f03d8-108">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f03d8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f03d8-109">EXAMPLES</span></span>

### <span data-ttu-id="f03d8-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f03d8-110">Example 1</span></span>
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

<span data-ttu-id="f03d8-111">T türü *SgxEnclave* Için kanıtlama sağlayıcı *pshtest* ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="f03d8-111">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="f03d8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f03d8-112">PARAMETERS</span></span>

### <span data-ttu-id="f03d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03d8-113">-DefaultProfile</span></span>
<span data-ttu-id="f03d8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f03d8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f03d8-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f03d8-115">-Name</span></span>
<span data-ttu-id="f03d8-116">Kiracının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f03d8-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="f03d8-117">Bu cmdlet, bu parametrenin belirttiği kiracı için kanıtlama ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="f03d8-117">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="f03d8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f03d8-118">-ResourceGroupName</span></span>
<span data-ttu-id="f03d8-119">Bir kanıt sağlayıcısının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f03d8-119">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="f03d8-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f03d8-120">-ResourceId</span></span>
<span data-ttu-id="f03d8-121">Bir kanıt sağlayıcısının RESOURCEID 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f03d8-121">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="f03d8-122">-T</span><span class="sxs-lookup"><span data-stu-id="f03d8-122">-Tee</span></span>
<span data-ttu-id="f03d8-123">Güvenilir yürütme ortamının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f03d8-123">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="f03d8-124">Dört tür ortamı destekliyoruz: SgxEnclave, Openenclaand, CyResComponent ve Vbsenclade.</span><span class="sxs-lookup"><span data-stu-id="f03d8-124">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="f03d8-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="f03d8-125">-Confirm</span></span>
<span data-ttu-id="f03d8-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f03d8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f03d8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f03d8-127">-WhatIf</span></span>
<span data-ttu-id="f03d8-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f03d8-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f03d8-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f03d8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f03d8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03d8-130">CommonParameters</span></span>
<span data-ttu-id="f03d8-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f03d8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03d8-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f03d8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03d8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f03d8-133">INPUTS</span></span>

### <span data-ttu-id="f03d8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f03d8-134">System.String</span></span>

## <span data-ttu-id="f03d8-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f03d8-135">OUTPUTS</span></span>

### <span data-ttu-id="f03d8-136">Microsoft. Azure. Commands. kanıtlama. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f03d8-136">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="f03d8-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f03d8-137">NOTES</span></span>

## <span data-ttu-id="f03d8-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f03d8-138">RELATED LINKS</span></span>
