---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: c00e8e8d33ef0f7b7b2591287e9bda9bc876e3c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107991"
---
# <span data-ttu-id="1a345-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1a345-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="1a345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a345-102">SYNOPSIS</span></span>
<span data-ttu-id="1a345-103">Azure API Yönetim hizmetini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="1a345-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="1a345-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a345-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a345-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a345-105">DESCRIPTION</span></span>

<span data-ttu-id="1a345-106">**Set-Azapsananaveya** cmdlet, BIR Azure API Yönetim hizmetini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1a345-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="1a345-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a345-107">EXAMPLES</span></span>

### <span data-ttu-id="1a345-108">Örnek 1: bir API yönetim hizmeti alma ve Premium 'a ölçeklendirme ve bölge ekleme</span><span class="sxs-lookup"><span data-stu-id="1a345-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="1a345-109">Bu örnekte bir API yönetim örneği alınır, bunu beş Premium birime ölçeklendirir ve Premium bölgeye ek üç birim ekler.</span><span class="sxs-lookup"><span data-stu-id="1a345-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="1a345-110">Örnek 2: güncelleştirme dağıtımı (dış VNET)</span><span class="sxs-lookup"><span data-stu-id="1a345-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="1a345-111">Bu komut, var olan bir API yönetim dağıtımını güncelleştirir ve bir dış *Vpntype* 'a katılır.</span><span class="sxs-lookup"><span data-stu-id="1a345-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="1a345-112">Örnek 3: Keykasa kaynağından parola kullanarak PsApiManagementCustomHostNameConfiguration örneğini oluşturma ve başlatma</span><span class="sxs-lookup"><span data-stu-id="1a345-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -SystemAssignedIdentity
```

### <span data-ttu-id="1a345-113">Örnek 4: Publisher e-postasını, NotificationSender e-postasını ve kuruluş adını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1a345-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="1a345-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a345-114">PARAMETERS</span></span>

### <span data-ttu-id="1a345-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="1a345-115">-AsJob</span></span>
<span data-ttu-id="1a345-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1a345-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a345-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a345-117">-DefaultProfile</span></span>
<span data-ttu-id="1a345-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a345-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a345-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a345-119">-InputObject</span></span>
<span data-ttu-id="1a345-120">Bir örnek</span><span class="sxs-lookup"><span data-stu-id="1a345-120">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="1a345-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1a345-121">-PassThru</span></span>
<span data-ttu-id="1a345-122">İşlem başarılı olursa, güncelleştirilmiş Psapımana'yi ardışık düzene gönderir.</span><span class="sxs-lookup"><span data-stu-id="1a345-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="1a345-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1a345-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="1a345-124">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu sunucu için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="1a345-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="1a345-125">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="1a345-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="1a345-126">Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak için Kullanıcı kimliklerini bu sunucuya atayın.</span><span class="sxs-lookup"><span data-stu-id="1a345-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a345-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="1a345-127">-Confirm</span></span>
<span data-ttu-id="1a345-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1a345-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a345-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a345-129">-WhatIf</span></span>
<span data-ttu-id="1a345-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a345-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a345-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1a345-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a345-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a345-132">CommonParameters</span></span>
<span data-ttu-id="1a345-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a345-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a345-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1a345-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a345-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a345-135">INPUTS</span></span>

### <span data-ttu-id="1a345-136">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="1a345-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1a345-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a345-137">OUTPUTS</span></span>

### <span data-ttu-id="1a345-138">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="1a345-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1a345-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a345-139">NOTES</span></span>

## <span data-ttu-id="1a345-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a345-140">RELATED LINKS</span></span>

[<span data-ttu-id="1a345-141">Get-Azıbir</span><span class="sxs-lookup"><span data-stu-id="1a345-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="1a345-142">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="1a345-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="1a345-143">Remove-azın</span><span class="sxs-lookup"><span data-stu-id="1a345-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
