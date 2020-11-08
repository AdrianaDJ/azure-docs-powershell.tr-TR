---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274309"
---
# <span data-ttu-id="a09a7-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a09a7-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="a09a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a09a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a09a7-103">Ağ sanal bir gereç kaynağına bağlı sanal bir gereç sitesini değiştirme veya değiştirme.</span><span class="sxs-lookup"><span data-stu-id="a09a7-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="a09a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a09a7-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a09a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a09a7-105">DESCRIPTION</span></span>
<span data-ttu-id="a09a7-106">Update-AzVirtualApplianceSite komutu sanal bir gereç sitesi kaynağını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a09a7-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="a09a7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a09a7-107">EXAMPLES</span></span>

### <span data-ttu-id="a09a7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a09a7-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="a09a7-109">Sanal bir gereç sitesi kaynağının adres önekini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="a09a7-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="a09a7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a09a7-110">PARAMETERS</span></span>

### <span data-ttu-id="a09a7-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="a09a7-111">-AddresssPrefix</span></span>
<span data-ttu-id="a09a7-112">Sitenin adres öneki.</span><span class="sxs-lookup"><span data-stu-id="a09a7-112">The address prefix for the site.</span></span>

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

### <span data-ttu-id="a09a7-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a09a7-113">-AsJob</span></span>
<span data-ttu-id="a09a7-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a09a7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a09a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09a7-115">-DefaultProfile</span></span>
<span data-ttu-id="a09a7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a09a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a09a7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a09a7-117">-Force</span></span>
<span data-ttu-id="a09a7-118">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="a09a7-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a09a7-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a09a7-119">-Name</span></span>
<span data-ttu-id="a09a7-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="a09a7-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a09a7-121">-Networkvirtualapplianceıd</span><span class="sxs-lookup"><span data-stu-id="a09a7-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="a09a7-122">Bu sitenin bağlı olduğu ağ sanal uygulaması.</span><span class="sxs-lookup"><span data-stu-id="a09a7-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="a09a7-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="a09a7-123">-O365Policy</span></span>
<span data-ttu-id="a09a7-124">Office 365 ayırıcı ilkesi.</span><span class="sxs-lookup"><span data-stu-id="a09a7-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a09a7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a09a7-125">-ResourceGroupName</span></span>
<span data-ttu-id="a09a7-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a09a7-126">The resource group name.</span></span>

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

### <span data-ttu-id="a09a7-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a09a7-127">-Tag</span></span>
<span data-ttu-id="a09a7-128">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="a09a7-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a09a7-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="a09a7-129">-Confirm</span></span>
<span data-ttu-id="a09a7-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a09a7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a09a7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a09a7-131">-WhatIf</span></span>
<span data-ttu-id="a09a7-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a09a7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a09a7-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a09a7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a09a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09a7-134">CommonParameters</span></span>
<span data-ttu-id="a09a7-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a09a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09a7-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a09a7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09a7-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a09a7-137">INPUTS</span></span>

### <span data-ttu-id="a09a7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a09a7-138">System.String</span></span>

### <span data-ttu-id="a09a7-139">Microsoft. Azure. Commands. Network. modeller. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="a09a7-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="a09a7-140">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a09a7-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a09a7-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a09a7-141">OUTPUTS</span></span>

### <span data-ttu-id="a09a7-142">Microsoft. Azure. Commands. Network. model. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="a09a7-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="a09a7-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a09a7-143">NOTES</span></span>

## <span data-ttu-id="a09a7-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a09a7-144">RELATED LINKS</span></span>
