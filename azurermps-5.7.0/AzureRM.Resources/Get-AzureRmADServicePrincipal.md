---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8344d9e794189d67a69c1be9a88e135b721a0d4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588802"
---
# <span data-ttu-id="33169-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33169-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="33169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33169-102">SYNOPSIS</span></span>
<span data-ttu-id="33169-103">Active Directory hizmet sorumlularına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="33169-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33169-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33169-104">SYNTAX</span></span>

### <span data-ttu-id="33169-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="33169-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33169-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="33169-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33169-107">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="33169-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33169-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="33169-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33169-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="33169-109">DESCRIPTION</span></span>
<span data-ttu-id="33169-110">Active Directory hizmet sorumlularına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="33169-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="33169-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33169-111">EXAMPLES</span></span>

### <span data-ttu-id="33169-112">SPN kullanarak hizmet sorumlularına filtre uygular</span><span class="sxs-lookup"><span data-stu-id="33169-112">Filters service principals using SPN</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="33169-113">Service sorumlularını 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN ile alır.</span><span class="sxs-lookup"><span data-stu-id="33169-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="33169-114">Arama dizesini kullanarak hizmet sorumlularına filtre uygular</span><span class="sxs-lookup"><span data-stu-id="33169-114">Filters service principals using Search String</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="33169-115">Görünen adı "Web" ile başlayan tüm ad hizmeti sorumlularına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="33169-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="33169-116">AD hizmeti sorumlularını listeleme</span><span class="sxs-lookup"><span data-stu-id="33169-116">List AD service principals</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="33169-117">Tüm reklam hizmeti sorumlularını alır.</span><span class="sxs-lookup"><span data-stu-id="33169-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="33169-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33169-118">PARAMETERS</span></span>

### <span data-ttu-id="33169-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33169-119">-DefaultProfile</span></span>
<span data-ttu-id="33169-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="33169-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33169-121">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="33169-121">-ObjectId</span></span>
<span data-ttu-id="33169-122">Hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="33169-122">Object id of the service principal.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33169-123">-SearchString</span><span class="sxs-lookup"><span data-stu-id="33169-123">-SearchString</span></span>
<span data-ttu-id="33169-124">Görünen adı bu değerle başlayan tüm hizmet sorumlularını getirir.</span><span class="sxs-lookup"><span data-stu-id="33169-124">Fetches all service principals that have the display name starting with this value.</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33169-125">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="33169-125">-ServicePrincipalName</span></span>
<span data-ttu-id="33169-126">Hizmetin SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="33169-126">SPN of the service.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33169-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33169-127">CommonParameters</span></span>
<span data-ttu-id="33169-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33169-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33169-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33169-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33169-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33169-130">INPUTS</span></span>

### <span data-ttu-id="33169-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="33169-131">None</span></span>
<span data-ttu-id="33169-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="33169-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33169-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33169-133">OUTPUTS</span></span>

### <span data-ttu-id="33169-134">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="33169-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="33169-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33169-135">NOTES</span></span>

## <span data-ttu-id="33169-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33169-136">RELATED LINKS</span></span>

[<span data-ttu-id="33169-137">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33169-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="33169-138">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33169-138">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="33169-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33169-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="33169-140">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="33169-140">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="33169-141">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="33169-141">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

