---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321898"
---
# <span data-ttu-id="90499-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="90499-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="90499-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90499-102">SYNOPSIS</span></span>
<span data-ttu-id="90499-103">Kanıtlamayı siler.</span><span class="sxs-lookup"><span data-stu-id="90499-103">Deletes an attestation.</span></span>

## <span data-ttu-id="90499-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90499-104">SYNTAX</span></span>

### <span data-ttu-id="90499-105">ByAvailableAttestation (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="90499-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90499-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="90499-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90499-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="90499-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90499-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="90499-108">DESCRIPTION</span></span>
<span data-ttu-id="90499-109">Remove-AzAttestation cmdlet 'i belirtilen kanıtlamayı siler.</span><span class="sxs-lookup"><span data-stu-id="90499-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="90499-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90499-110">EXAMPLES</span></span>

### <span data-ttu-id="90499-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="90499-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="90499-112">*PSH-test-RG* adlı kaynak grubundaki *Pshtest3* adındaki kanıtlama sağlayıcısını geçerli abonelikten silin.</span><span class="sxs-lookup"><span data-stu-id="90499-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="90499-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90499-113">PARAMETERS</span></span>

### <span data-ttu-id="90499-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90499-114">-DefaultProfile</span></span>
<span data-ttu-id="90499-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90499-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90499-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90499-116">-InputObject</span></span>
<span data-ttu-id="90499-117">Silinecek kanıtlama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="90499-117">Attestation object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Attestation.Models.PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90499-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="90499-118">-Name</span></span>
<span data-ttu-id="90499-119">Kaldırılacak kanıtlama adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90499-119">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90499-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="90499-120">-PassThru</span></span>
<span data-ttu-id="90499-121">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="90499-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="90499-122">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="90499-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="90499-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90499-123">-ResourceGroupName</span></span>
<span data-ttu-id="90499-124">Kaldırılacak Azure kanıtlama kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90499-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90499-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="90499-125">-ResourceId</span></span>
<span data-ttu-id="90499-126">Kanıtlama kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="90499-126">Attestation Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90499-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="90499-127">-Confirm</span></span>
<span data-ttu-id="90499-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90499-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90499-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90499-129">-WhatIf</span></span>
<span data-ttu-id="90499-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90499-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90499-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90499-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90499-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90499-132">CommonParameters</span></span>
<span data-ttu-id="90499-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90499-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90499-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="90499-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90499-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90499-135">INPUTS</span></span>

### <span data-ttu-id="90499-136">System. String</span><span class="sxs-lookup"><span data-stu-id="90499-136">System.String</span></span>

### <span data-ttu-id="90499-137">Microsoft. Azure. Commands. kanıtlama. modeller. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="90499-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="90499-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90499-138">OUTPUTS</span></span>

### <span data-ttu-id="90499-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90499-139">System.Boolean</span></span>

## <span data-ttu-id="90499-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90499-140">NOTES</span></span>

## <span data-ttu-id="90499-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90499-141">RELATED LINKS</span></span>
