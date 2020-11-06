---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 853404bce6d45f2824c574b249c434ccebc281ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593430"
---
# <span data-ttu-id="21108-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21108-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="21108-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21108-102">SYNOPSIS</span></span>
<span data-ttu-id="21108-103">Var olan bir Azure Active Directory hizmet sorumlusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="21108-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21108-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21108-104">SYNTAX</span></span>

### <span data-ttu-id="21108-105">Spobjectivseçwithdisplaynameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="21108-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21108-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="21108-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21108-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="21108-107">DESCRIPTION</span></span>
<span data-ttu-id="21108-108">Var olan bir Azure Active Directory hizmet sorumlusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="21108-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="21108-109">Bu hizmet sorumlusunun ilişkili kimlik bilgilerini güncelleştirmek için lütfen New-AzureRmADSpCredential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="21108-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="21108-110">Temel uygulamayla ilişkili özellikleri güncelleştirmek için lütfen Set-AzureRmADApplication cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="21108-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="21108-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21108-111">EXAMPLES</span></span>

### <span data-ttu-id="21108-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="21108-112">Example 1</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="21108-113">Belirtilen nesne kimliğine sahip hizmet sorumlusunun görünen adını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="21108-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="21108-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="21108-114">Example 2</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="21108-115">Belirtilen hizmet asıl adına sahip hizmet sorumlusunun görünen adını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="21108-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="21108-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21108-116">PARAMETERS</span></span>

### <span data-ttu-id="21108-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21108-117">-DefaultProfile</span></span>
<span data-ttu-id="21108-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="21108-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21108-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="21108-119">-DisplayName</span></span>
<span data-ttu-id="21108-120">Hizmet sorumlusu için yeni görünen ad.</span><span class="sxs-lookup"><span data-stu-id="21108-120">New display name for the service principal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21108-121">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="21108-121">-ObjectId</span></span>
<span data-ttu-id="21108-122">Güncelleştirilecek hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="21108-122">The object id of the service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21108-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="21108-123">-ServicePrincipalName</span></span>
<span data-ttu-id="21108-124">Güncelleştirilecek hizmet sorumlusu SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="21108-124">The SPN of service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21108-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="21108-125">-Confirm</span></span>
<span data-ttu-id="21108-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="21108-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21108-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21108-127">-WhatIf</span></span>
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

### <span data-ttu-id="21108-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21108-128">CommonParameters</span></span>
<span data-ttu-id="21108-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21108-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21108-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21108-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21108-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21108-131">INPUTS</span></span>

### <span data-ttu-id="21108-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="21108-132">None</span></span>
<span data-ttu-id="21108-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="21108-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21108-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21108-134">OUTPUTS</span></span>

## <span data-ttu-id="21108-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21108-135">NOTES</span></span>

## <span data-ttu-id="21108-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21108-136">RELATED LINKS</span></span>

[<span data-ttu-id="21108-137">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21108-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="21108-138">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21108-138">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="21108-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21108-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="21108-140">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="21108-140">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="21108-141">Yeni-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="21108-141">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="21108-142">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="21108-142">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

