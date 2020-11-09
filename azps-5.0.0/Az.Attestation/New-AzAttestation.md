---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321901"
---
# <span data-ttu-id="bc011-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="bc011-101">New-AzAttestation</span></span>

## <span data-ttu-id="bc011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc011-102">SYNOPSIS</span></span>
<span data-ttu-id="bc011-103">Kanıt oluşturur</span><span class="sxs-lookup"><span data-stu-id="bc011-103">Creates an attestation</span></span>

## <span data-ttu-id="bc011-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc011-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc011-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc011-105">DESCRIPTION</span></span>
<span data-ttu-id="bc011-106">New-AzAttestation cmdlet 'i belirtilen kaynak grubunda bir kanıt oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc011-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="bc011-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc011-107">EXAMPLES</span></span>

### <span data-ttu-id="bc011-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bc011-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest4 -ResourceGroupName psh-test-rg -Location "East US" -Tags @{Test="true";CreationYear="2020"}                                                                                                                                                                                         
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest4
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest4
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest4.us.attest.azure.net
Tags              : {CreationYear, Test}
TagsTable         :
                    Name          Value
                    ============  =====
                    CreationYear  2020
                    Test          true
```

<span data-ttu-id="bc011-109">Birkaç etiketli *pshtest4* adlı bir kanıt sağlayıcısının yeni örneğini oluşturun ve bu Ilke için AAD güveni 'ni kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc011-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="bc011-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bc011-110">Example 2</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg -Location "East US" -PolicySignersCertificateFile .\cert1.pem                                                                                                                                                
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest3
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest3
Status            : Ready
TrustModel        : Isolated
AttestUri         : https://pshtest3.us.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="bc011-111">Bir PEM dosyası aracılığıyla güvenilir bir imza anahtarı kümesi belirleyerek, yönetim için ısoded güveni kullanan, *pshtest3* ' adlı bir kanıt sağlayıcısının yeni örneğini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bc011-111">Create a new instance of an Attestation Provider named *pshtest3* \` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="bc011-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc011-112">PARAMETERS</span></span>

### <span data-ttu-id="bc011-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc011-113">-DefaultProfile</span></span>
<span data-ttu-id="bc011-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc011-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc011-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="bc011-115">-Location</span></span>
<span data-ttu-id="bc011-116">Kanıtlama sağlayıcısının oluşturulacağı Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc011-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="bc011-117">Seçimlerinizi görmek için komut Get-AzResourceProvider ProviderNamespace parametresiyle birlikte kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc011-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc011-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="bc011-118">-Name</span></span>
<span data-ttu-id="bc011-119">Oluşturulacak örnek adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc011-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="bc011-120">Ad, harf, sayı veya kısa çizgi bileşimleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="bc011-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="bc011-121">Ad bir harfle veya rakamla başlamalıdır ve bitmelidir.</span><span class="sxs-lookup"><span data-stu-id="bc011-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="bc011-122">Ad, evrensel olarak benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc011-122">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc011-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="bc011-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="bc011-124">Tek bir sertifika dosyasındaki verme ilkesi için güvenilen İmzalama anahtarları kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc011-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc011-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc011-125">-ResourceGroupName</span></span>
<span data-ttu-id="bc011-126">Kanıtlamayı oluşturacağınız varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc011-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc011-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bc011-127">-Tag</span></span>
<span data-ttu-id="bc011-128">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="bc011-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc011-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc011-129">-Confirm</span></span>
<span data-ttu-id="bc011-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc011-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc011-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc011-131">-WhatIf</span></span>
<span data-ttu-id="bc011-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc011-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc011-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc011-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc011-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc011-134">CommonParameters</span></span>
<span data-ttu-id="bc011-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc011-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc011-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bc011-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc011-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc011-137">INPUTS</span></span>

### <span data-ttu-id="bc011-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bc011-138">System.String</span></span>

### <span data-ttu-id="bc011-139">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc011-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bc011-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc011-140">OUTPUTS</span></span>

### <span data-ttu-id="bc011-141">Microsoft. Azure. Commands. kanıtlama. modeller. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="bc011-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="bc011-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc011-142">NOTES</span></span>

## <span data-ttu-id="bc011-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc011-143">RELATED LINKS</span></span>
