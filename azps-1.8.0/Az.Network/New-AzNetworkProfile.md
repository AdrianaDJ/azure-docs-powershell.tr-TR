---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: 87d753ebaf2d8d4891fc96dbc25f7ad0fa1095af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760307"
---
# <span data-ttu-id="678d8-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="678d8-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="678d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="678d8-102">SYNOPSIS</span></span>
<span data-ttu-id="678d8-103">Yeni ağ profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="678d8-103">Creates a new network profile.</span></span>

## <span data-ttu-id="678d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="678d8-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="678d8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="678d8-105">DESCRIPTION</span></span>
<span data-ttu-id="678d8-106">**New-AzNetworkProfile** cmdlet 'i, yeni bir ağ profili üst düzey kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="678d8-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="678d8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="678d8-107">EXAMPLES</span></span>

### <span data-ttu-id="678d8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="678d8-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="678d8-109">Bu, yeni bir ağ profili üst düzey kaynağı oluşturur</span><span class="sxs-lookup"><span data-stu-id="678d8-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="678d8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="678d8-110">PARAMETERS</span></span>

### <span data-ttu-id="678d8-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="678d8-111">-AsJob</span></span>
<span data-ttu-id="678d8-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="678d8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="678d8-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="678d8-113">-ContainerNicConfig</span></span>
<span data-ttu-id="678d8-114">Bu ağ profiline eklenecek kapsayıcı ağ arabirimi yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="678d8-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678d8-115">-DefaultProfile</span></span>
<span data-ttu-id="678d8-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="678d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="678d8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="678d8-117">-Force</span></span>
<span data-ttu-id="678d8-118">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="678d8-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="678d8-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="678d8-119">-Location</span></span>
<span data-ttu-id="678d8-120">Konum.</span><span class="sxs-lookup"><span data-stu-id="678d8-120">The location.</span></span>

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

### <span data-ttu-id="678d8-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="678d8-121">-Name</span></span>
<span data-ttu-id="678d8-122">Ağ profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="678d8-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="678d8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="678d8-123">-ResourceGroupName</span></span>
<span data-ttu-id="678d8-124">Ağ profilinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="678d8-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="678d8-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="678d8-125">-Tag</span></span>
<span data-ttu-id="678d8-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="678d8-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="678d8-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="678d8-127">-Confirm</span></span>
<span data-ttu-id="678d8-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="678d8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="678d8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="678d8-129">-WhatIf</span></span>
<span data-ttu-id="678d8-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="678d8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="678d8-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="678d8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="678d8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678d8-132">CommonParameters</span></span>
<span data-ttu-id="678d8-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="678d8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678d8-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678d8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678d8-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="678d8-135">INPUTS</span></span>

### <span data-ttu-id="678d8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="678d8-136">System.String</span></span>

### <span data-ttu-id="678d8-137">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="678d8-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="678d8-138">Microsoft. Azure. Commands. Network. model. Pscontainernetworkınterfaceconfiguration []</span><span class="sxs-lookup"><span data-stu-id="678d8-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="678d8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="678d8-139">OUTPUTS</span></span>

### <span data-ttu-id="678d8-140">Microsoft. Azure. Commands. Network. modeller. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="678d8-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="678d8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="678d8-141">NOTES</span></span>

## <span data-ttu-id="678d8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="678d8-142">RELATED LINKS</span></span>

[<span data-ttu-id="678d8-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="678d8-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="678d8-144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="678d8-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="678d8-145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="678d8-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)