---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 997e1150549ac219c54e42fdd4c7674cd53d5ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753360"
---
# <span data-ttu-id="b80c0-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="b80c0-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="b80c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b80c0-102">SYNOPSIS</span></span>
<span data-ttu-id="b80c0-103">Kanıtlamayı siler.</span><span class="sxs-lookup"><span data-stu-id="b80c0-103">Deletes an attestation.</span></span>

## <span data-ttu-id="b80c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b80c0-104">SYNTAX</span></span>

### <span data-ttu-id="b80c0-105">ByAvailableAttestation (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b80c0-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b80c0-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="b80c0-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b80c0-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="b80c0-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b80c0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b80c0-108">DESCRIPTION</span></span>
<span data-ttu-id="b80c0-109">Remove-AzAttestation cmdlet 'i belirtilen kanıtlamayı siler.</span><span class="sxs-lookup"><span data-stu-id="b80c0-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="b80c0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b80c0-110">EXAMPLES</span></span>

### <span data-ttu-id="b80c0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b80c0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name example -ResourceGroupName rg1 
```

<span data-ttu-id="b80c0-112">Geçerli aboneliğin ve "RG1" kaynak grubundan "örnek" kanıtlamayı silme.</span><span class="sxs-lookup"><span data-stu-id="b80c0-112">Delete Attestation "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="b80c0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b80c0-113">PARAMETERS</span></span>

### <span data-ttu-id="b80c0-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="b80c0-114">-AsJob</span></span>
<span data-ttu-id="b80c0-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b80c0-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b80c0-116">-DefaultProfile</span></span>
<span data-ttu-id="b80c0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b80c0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b80c0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b80c0-118">-InputObject</span></span>
<span data-ttu-id="b80c0-119">Silinecek kanıtlama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b80c0-119">Attestation object to be deleted.</span></span>

```yaml
Type: PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b80c0-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b80c0-120">-Name</span></span>
<span data-ttu-id="b80c0-121">Kaldırılacak kanıtlama adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b80c0-121">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80c0-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b80c0-122">-PassThru</span></span>
<span data-ttu-id="b80c0-123">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="b80c0-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b80c0-124">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="b80c0-124">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80c0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b80c0-125">-ResourceGroupName</span></span>
<span data-ttu-id="b80c0-126">Kaldırılacak Azure kanıtlama kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b80c0-126">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80c0-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b80c0-127">-ResourceId</span></span>
<span data-ttu-id="b80c0-128">Kanıtlama kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b80c0-128">Attestation Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b80c0-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="b80c0-129">-Confirm</span></span>
<span data-ttu-id="b80c0-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b80c0-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80c0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b80c0-131">-WhatIf</span></span>
<span data-ttu-id="b80c0-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b80c0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b80c0-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b80c0-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b80c0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b80c0-134">CommonParameters</span></span>
<span data-ttu-id="b80c0-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b80c0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b80c0-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b80c0-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b80c0-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b80c0-137">INPUTS</span></span>

### <span data-ttu-id="b80c0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b80c0-138">System.String</span></span>

### <span data-ttu-id="b80c0-139">Microsoft. Azure. Commands. kanıtlama. modeller. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="b80c0-139">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="b80c0-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b80c0-140">OUTPUTS</span></span>

### <span data-ttu-id="b80c0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b80c0-141">System.Boolean</span></span>

## <span data-ttu-id="b80c0-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b80c0-142">NOTES</span></span>

## <span data-ttu-id="b80c0-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b80c0-143">RELATED LINKS</span></span>
