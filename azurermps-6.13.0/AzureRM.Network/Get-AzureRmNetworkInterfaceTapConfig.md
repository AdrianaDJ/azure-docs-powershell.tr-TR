---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2f6c4f410c7d4f92c8dcd911e0c113f2a91b304c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765093"
---
# <span data-ttu-id="e2fb4-101">Get-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e2fb4-101">Get-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="e2fb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="e2fb4-103">Bir dokunuş yapılandırma kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-103">Gets a Tap configuration resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2fb4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2fb4-104">SYNTAX</span></span>

### <span data-ttu-id="e2fb4-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e2fb4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2fb4-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e2fb4-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2fb4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2fb4-107">DESCRIPTION</span></span>
<span data-ttu-id="e2fb4-108">**Get-Azurermnetworkınterfacetapconfig** cmdlet 'i, belirli bir kaynak grubu Için bir Azure dokunma yapılandırması alır, ağ arabirimi</span><span class="sxs-lookup"><span data-stu-id="e2fb4-108">The **Get-AzureRmNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="e2fb4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2fb4-109">EXAMPLES</span></span>

### <span data-ttu-id="e2fb4-110">Örnek 1: belirli bir ağ arabiriminin tüm dokunma yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="e2fb4-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="e2fb4-111">Bu komut, verilen ağ arabirimine eklenecek yapılandırmalara dokunun.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="e2fb4-112">Örnek 2: belirli bir dokunma yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="e2fb4-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="e2fb4-113">Bu komut, belirli bir ağ arabirimine belirli dokunuş yapılandırmasını getirir.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-113">This command gets specific tap configuration added for the given network interface.</span></span>

## <span data-ttu-id="e2fb4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2fb4-114">PARAMETERS</span></span>

### <span data-ttu-id="e2fb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2fb4-115">-DefaultProfile</span></span>
<span data-ttu-id="e2fb4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2fb4-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2fb4-117">-Name</span></span>
<span data-ttu-id="e2fb4-118">Belirli dokunun yapılandırması adı.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-118">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2fb4-119">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="e2fb4-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="e2fb4-120">Ağ arabirim adı.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-120">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2fb4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2fb4-121">-ResourceGroupName</span></span>
<span data-ttu-id="e2fb4-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2fb4-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e2fb4-123">-ResourceId</span></span>
<span data-ttu-id="e2fb4-124">TapConfiguration kaynağının RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e2fb4-124">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2fb4-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="e2fb4-125">-Confirm</span></span>
<span data-ttu-id="e2fb4-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2fb4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2fb4-127">-WhatIf</span></span>
<span data-ttu-id="e2fb4-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2fb4-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2fb4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2fb4-130">CommonParameters</span></span>
<span data-ttu-id="e2fb4-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2fb4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2fb4-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2fb4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2fb4-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2fb4-133">INPUTS</span></span>

### <span data-ttu-id="e2fb4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e2fb4-134">System.String</span></span>

## <span data-ttu-id="e2fb4-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2fb4-135">OUTPUTS</span></span>

### <span data-ttu-id="e2fb4-136">Microsoft. Azure. Commands. Network. model. Psnetworkınterfacetapconfiguration</span><span class="sxs-lookup"><span data-stu-id="e2fb4-136">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="e2fb4-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2fb4-137">NOTES</span></span>

## <span data-ttu-id="e2fb4-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2fb4-138">RELATED LINKS</span></span>
