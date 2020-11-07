---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
ms.openlocfilehash: 3831be3072f6922ad986cbde5a0a800764d1656a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763499"
---
# <span data-ttu-id="ffa25-101">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="ffa25-101">Set-AzureRmApiManagement</span></span>

## <span data-ttu-id="ffa25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa25-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa25-103">Azure API Yönetim hizmetini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="ffa25-103">Updates an Azure Api Management service</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffa25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ffa25-104">SYNTAX</span></span>

```
Set-AzureRmApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa25-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ffa25-105">DESCRIPTION</span></span>

<span data-ttu-id="ffa25-106">**Set-Azurermapsananaks** cmdlet 'ı BIR Azure API Yönetim hizmetini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ffa25-106">The **Set-AzureRmApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="ffa25-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ffa25-107">EXAMPLES</span></span>

### <span data-ttu-id="ffa25-108">Örnek 1 bir API yönetim hizmeti alma ve Premium 'a ölçeklendirme ve bölge ekleme</span><span class="sxs-lookup"><span data-stu-id="ffa25-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="ffa25-109">Bu örnekte bir API yönetim örneği alınır, bunu beş Premium birime ölçeklendirir ve Premium bölgeye ek üç birim ekler.</span><span class="sxs-lookup"><span data-stu-id="ffa25-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="ffa25-110">Örnek 2: güncelleştirme dağıtımı (dış VNET)</span><span class="sxs-lookup"><span data-stu-id="ffa25-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="ffa25-111">Bu komut, var olan bir API yönetim dağıtımını güncelleştirir ve bir dış *Vpntype* 'a katılır.</span><span class="sxs-lookup"><span data-stu-id="ffa25-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="ffa25-112">Örnek 3: Keykasa kaynağından parola kullanarak PsApiManagementCustomHostNameConfiguration örneğini oluşturma ve başlatma</span><span class="sxs-lookup"><span data-stu-id="ffa25-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzureRmApiManagement -InputObject $apim -AssignIdentity
```

## <span data-ttu-id="ffa25-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ffa25-113">PARAMETERS</span></span>

### <span data-ttu-id="ffa25-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="ffa25-114">-AsJob</span></span>
<span data-ttu-id="ffa25-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ffa25-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffa25-116">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="ffa25-116">-AssignIdentity</span></span>
<span data-ttu-id="ffa25-117">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu sunucu için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="ffa25-117">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ffa25-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa25-118">-DefaultProfile</span></span>
<span data-ttu-id="ffa25-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ffa25-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa25-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffa25-120">-InputObject</span></span>
<span data-ttu-id="ffa25-121">Bir örnek</span><span class="sxs-lookup"><span data-stu-id="ffa25-121">The ApiManagement instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa25-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ffa25-122">-PassThru</span></span>
<span data-ttu-id="ffa25-123">İşlem başarılı olursa, güncelleştirilmiş Psapımana'yi ardışık düzene gönderir.</span><span class="sxs-lookup"><span data-stu-id="ffa25-123">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="ffa25-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="ffa25-124">-Confirm</span></span>
<span data-ttu-id="ffa25-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ffa25-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa25-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa25-126">-WhatIf</span></span>
<span data-ttu-id="ffa25-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ffa25-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffa25-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ffa25-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa25-129">CommonParameters</span></span>
<span data-ttu-id="ffa25-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ffa25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa25-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffa25-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa25-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ffa25-132">INPUTS</span></span>

### <span data-ttu-id="ffa25-133">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="ffa25-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="ffa25-134">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ffa25-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ffa25-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ffa25-135">OUTPUTS</span></span>

### <span data-ttu-id="ffa25-136">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="ffa25-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ffa25-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ffa25-137">NOTES</span></span>

## <span data-ttu-id="ffa25-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ffa25-138">RELATED LINKS</span></span>

[<span data-ttu-id="ffa25-139">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="ffa25-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="ffa25-140">Yeni-azurermapı</span><span class="sxs-lookup"><span data-stu-id="ffa25-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="ffa25-141">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="ffa25-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)