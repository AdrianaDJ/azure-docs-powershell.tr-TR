---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkProfile.md
ms.openlocfilehash: fedf6818f95bd5afadb92c1423a1dbb3296727e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590144"
---
# <span data-ttu-id="54b42-101">New-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="54b42-101">New-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="54b42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54b42-102">SYNOPSIS</span></span>
<span data-ttu-id="54b42-103">Yeni ağ profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54b42-103">Creates a new network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54b42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54b42-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54b42-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="54b42-105">DESCRIPTION</span></span>
<span data-ttu-id="54b42-106">**Yeni-AzureRmNetworkProfile** cmdlet 'i, yeni bir ağ profili üst düzey kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54b42-106">The **New-AzureRmNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="54b42-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54b42-107">EXAMPLES</span></span>

### <span data-ttu-id="54b42-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="54b42-108">Example 1</span></span>
```powershell
$networkProfile = New-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="54b42-109">Bu, yeni bir ağ profili üst düzey kaynağı oluşturur</span><span class="sxs-lookup"><span data-stu-id="54b42-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="54b42-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54b42-110">PARAMETERS</span></span>

### <span data-ttu-id="54b42-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="54b42-111">-AsJob</span></span>
<span data-ttu-id="54b42-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="54b42-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54b42-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="54b42-113">-ContainerNicConfig</span></span>
<span data-ttu-id="54b42-114">Bu ağ profiline eklenecek kapsayıcı ağ arabirimi yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="54b42-114">The container network interface configurations to add to this network profile.</span></span>

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

### <span data-ttu-id="54b42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b42-115">-DefaultProfile</span></span>
<span data-ttu-id="54b42-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54b42-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54b42-117">-Force</span><span class="sxs-lookup"><span data-stu-id="54b42-117">-Force</span></span>
<span data-ttu-id="54b42-118">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="54b42-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="54b42-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="54b42-119">-Location</span></span>
<span data-ttu-id="54b42-120">Konum.</span><span class="sxs-lookup"><span data-stu-id="54b42-120">The location.</span></span>

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

### <span data-ttu-id="54b42-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="54b42-121">-Name</span></span>
<span data-ttu-id="54b42-122">Ağ profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="54b42-122">The name of the network profile.</span></span>

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

### <span data-ttu-id="54b42-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54b42-123">-ResourceGroupName</span></span>
<span data-ttu-id="54b42-124">Ağ profilinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="54b42-124">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="54b42-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="54b42-125">-Tag</span></span>
<span data-ttu-id="54b42-126">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="54b42-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="54b42-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="54b42-127">-Confirm</span></span>
<span data-ttu-id="54b42-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54b42-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54b42-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54b42-129">-WhatIf</span></span>
<span data-ttu-id="54b42-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54b42-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54b42-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54b42-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54b42-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b42-132">CommonParameters</span></span>
<span data-ttu-id="54b42-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54b42-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b42-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54b42-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b42-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54b42-135">INPUTS</span></span>

### <span data-ttu-id="54b42-136">System. String</span><span class="sxs-lookup"><span data-stu-id="54b42-136">System.String</span></span>

### <span data-ttu-id="54b42-137">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="54b42-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="54b42-138">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. Pscontainernetworkınterface, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="54b42-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterface, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="54b42-139">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. Pscontainernetworkınterfaceconfiguration, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="54b42-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="54b42-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54b42-140">OUTPUTS</span></span>

### <span data-ttu-id="54b42-141">Microsoft. Azure. Commands. Network. modeller. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="54b42-141">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="54b42-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54b42-142">NOTES</span></span>

## <span data-ttu-id="54b42-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54b42-143">RELATED LINKS</span></span>
