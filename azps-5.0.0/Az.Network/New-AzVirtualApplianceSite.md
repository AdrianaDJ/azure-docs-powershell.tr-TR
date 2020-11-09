---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325888"
---
# <span data-ttu-id="51269-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="51269-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="51269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51269-102">SYNOPSIS</span></span>
<span data-ttu-id="51269-103">Ağ sanal bir gereç ile bağlantılı bir site oluşturun.</span><span class="sxs-lookup"><span data-stu-id="51269-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="51269-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51269-104">SYNTAX</span></span>

### <span data-ttu-id="51269-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51269-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51269-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="51269-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51269-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="51269-107">DESCRIPTION</span></span>
<span data-ttu-id="51269-108">New-AzVirtualApplianceSite komutu, ağ sanal bir gereç kaynağına bağlı sanal bir gereç sitesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="51269-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="51269-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51269-109">EXAMPLES</span></span>

### <span data-ttu-id="51269-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="51269-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="51269-111">Kaynak grubunda yeni bir Sanal Gereç sitesi oluşturun: latestrg.</span><span class="sxs-lookup"><span data-stu-id="51269-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="51269-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51269-112">PARAMETERS</span></span>

### <span data-ttu-id="51269-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="51269-113">-AddressPrefix</span></span>
<span data-ttu-id="51269-114">Sitenin adres öneki.</span><span class="sxs-lookup"><span data-stu-id="51269-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="51269-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="51269-115">-AsJob</span></span>
<span data-ttu-id="51269-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="51269-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51269-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51269-117">-DefaultProfile</span></span>
<span data-ttu-id="51269-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51269-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51269-119">-Force</span><span class="sxs-lookup"><span data-stu-id="51269-119">-Force</span></span>
<span data-ttu-id="51269-120">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="51269-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="51269-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="51269-121">-Name</span></span>
<span data-ttu-id="51269-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="51269-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51269-123">-Networkvirtualapplianceıd</span><span class="sxs-lookup"><span data-stu-id="51269-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="51269-124">Bu sitenin bağlı olduğu ağ sanal uygulaması.</span><span class="sxs-lookup"><span data-stu-id="51269-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="51269-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="51269-125">-O365Policy</span></span>
<span data-ttu-id="51269-126">Office 365 ayırıcı ilkesi.</span><span class="sxs-lookup"><span data-stu-id="51269-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51269-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51269-127">-ResourceGroupName</span></span>
<span data-ttu-id="51269-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="51269-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51269-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="51269-129">-ResourceId</span></span>
<span data-ttu-id="51269-130">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="51269-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51269-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="51269-131">-Tag</span></span>
<span data-ttu-id="51269-132">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="51269-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="51269-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="51269-133">-Confirm</span></span>
<span data-ttu-id="51269-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="51269-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51269-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51269-135">-WhatIf</span></span>
<span data-ttu-id="51269-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="51269-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51269-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="51269-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51269-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51269-138">CommonParameters</span></span>
<span data-ttu-id="51269-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51269-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51269-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="51269-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51269-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51269-141">INPUTS</span></span>

### <span data-ttu-id="51269-142">System. String</span><span class="sxs-lookup"><span data-stu-id="51269-142">System.String</span></span>

### <span data-ttu-id="51269-143">Microsoft. Azure. Commands. Network. modeller. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="51269-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="51269-144">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="51269-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="51269-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51269-145">OUTPUTS</span></span>

### <span data-ttu-id="51269-146">Microsoft. Azure. Commands. Network. model. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="51269-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="51269-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51269-147">NOTES</span></span>

## <span data-ttu-id="51269-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51269-148">RELATED LINKS</span></span>
