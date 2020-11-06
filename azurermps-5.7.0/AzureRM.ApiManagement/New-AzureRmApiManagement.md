---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594154"
---
# <span data-ttu-id="a1e2a-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="a1e2a-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="a1e2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e2a-103">Bir API yönetim dağıtımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1e2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1e2a-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1e2a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1e2a-105">DESCRIPTION</span></span>
<span data-ttu-id="a1e2a-106">**Yeni-Azurermapsanana,** Azure API YÖNETIMINDE bir API yönetim dağıtımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="a1e2a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1e2a-107">EXAMPLES</span></span>

### <span data-ttu-id="a1e2a-108">Örnek 1: Geliştirici katmanı API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="a1e2a-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="a1e2a-109">Bu komut bir geliştirici katmanı API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="a1e2a-110">Bu komut, organizasyonu ve yönetici adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="a1e2a-111">Komut *SKU* parametresini belirtmez.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="a1e2a-112">Bu nedenle, cmdlet geliştirici varsayılan değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="a1e2a-113">Örnek 2: üç birimli standart bir katman hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="a1e2a-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="a1e2a-114">Bu komut, üç birimli bir standart katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="a1e2a-115">Örnek 3: dış sanal ağ için API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="a1e2a-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="a1e2a-116">Bu komut, bir Azure sanal ağ alt ağında, Batı ABD 'deki ana bölgeyle birlikte dış bir ağ geçidi uç noktası içeren bir Premium katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="a1e2a-117">Örnek 4: iç sanal ağ için bir API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="a1e2a-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="a1e2a-118">Bu komut, bir Azure sanal ağ alt ağında, Batı ABD 'deki ana bölgeyle birlikte dahili bir ağ geçidi uç noktası içeren bir Premium katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="a1e2a-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1e2a-119">PARAMETERS</span></span>

### <span data-ttu-id="a1e2a-120">-Additionalbölgelerle</span><span class="sxs-lookup"><span data-stu-id="a1e2a-120">-AdditionalRegions</span></span>
<span data-ttu-id="a1e2a-121">Azure API yönetimi için ek dağıtım bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e2a-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="a1e2a-122">-AdminEmail</span></span>
<span data-ttu-id="a1e2a-123">API yönetim sisteminin gönderdiği tüm bildirimler için kaynak e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="a1e2a-124">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="a1e2a-124">-Capacity</span></span>
<span data-ttu-id="a1e2a-125">Azure API yönetim hizmetinin SKU kapasitesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="a1e2a-126">Varsayılan değer bir (1).</span><span class="sxs-lookup"><span data-stu-id="a1e2a-126">The default is one (1).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e2a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e2a-127">-DefaultProfile</span></span>
<span data-ttu-id="a1e2a-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a1e2a-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="a1e2a-129">-Location</span></span>
<span data-ttu-id="a1e2a-130">API Yönetim hizmetini oluşturacağınız konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-130">Specifies the location to create the Api Management service.</span></span>

<span data-ttu-id="a1e2a-131">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="a1e2a-131">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="a1e2a-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1e2a-132">-Name</span></span>
<span data-ttu-id="a1e2a-133">API yönetim dağıtımı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-133">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="a1e2a-134">-Kuruluş</span><span class="sxs-lookup"><span data-stu-id="a1e2a-134">-Organization</span></span>
<span data-ttu-id="a1e2a-135">Kuruluşun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-135">Specifies the name of an organization.</span></span>
<span data-ttu-id="a1e2a-136">API Yönetimi, bu adresi Geliştirici Portalında e-posta bildirimlerinde kullanır.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-136">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="a1e2a-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e2a-137">-ResourceGroupName</span></span>
<span data-ttu-id="a1e2a-138">Bu cmdlet 'in API yönetim dağıtımını oluşturduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-138">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="a1e2a-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="a1e2a-139">-Sku</span></span>
<span data-ttu-id="a1e2a-140">API yönetim hizmetinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-140">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="a1e2a-141">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a1e2a-141">Valid values are:</span></span> 

- <span data-ttu-id="a1e2a-142">İyle</span><span class="sxs-lookup"><span data-stu-id="a1e2a-142">Developer</span></span> 
- <span data-ttu-id="a1e2a-143">Ardından</span><span class="sxs-lookup"><span data-stu-id="a1e2a-143">Standard</span></span> 
- <span data-ttu-id="a1e2a-144">Min</span><span class="sxs-lookup"><span data-stu-id="a1e2a-144">Premium</span></span> 

<span data-ttu-id="a1e2a-145">Varsayılan olarak geliştirici kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-145">The default is Developer.</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e2a-146">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a1e2a-146">-Tag</span></span>
<span data-ttu-id="a1e2a-147">Etiket sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-147">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e2a-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a1e2a-148">-VirtualNetwork</span></span>
<span data-ttu-id="a1e2a-149">Master Azure API yönetim dağıtım bölgesinin sanal ağ yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-149">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e2a-150">-VpnType</span><span class="sxs-lookup"><span data-stu-id="a1e2a-150">-VpnType</span></span>
<span data-ttu-id="a1e2a-151">Sanal ağ 'ın sanal ağ türü.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-151">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="a1e2a-152">Geçerli değerler</span><span class="sxs-lookup"><span data-stu-id="a1e2a-152">Valid Values are</span></span> 
- <span data-ttu-id="a1e2a-153">"None" (varsayılan değer.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-153">"None" (Default Value.</span></span> <span data-ttu-id="a1e2a-154">Herhangi bir sanal ağın parçası değildir ")</span><span class="sxs-lookup"><span data-stu-id="a1e2a-154">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="a1e2a-155">"Dış" (bir Internet 'e yönelik uç noktaya sahip bir sanal ağın içinde bir kuruluş)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-155">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="a1e2a-156">"İç" (bir sanal ağın iç uç noktasına sahip olduğu bir sanal ağ içinde, kuruluş)</span><span class="sxs-lookup"><span data-stu-id="a1e2a-156">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1e2a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e2a-157">CommonParameters</span></span>
<span data-ttu-id="a1e2a-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e2a-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1e2a-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e2a-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1e2a-160">INPUTS</span></span>

### <span data-ttu-id="a1e2a-161">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a1e2a-161">None</span></span>
<span data-ttu-id="a1e2a-162">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a1e2a-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1e2a-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1e2a-163">OUTPUTS</span></span>

### <span data-ttu-id="a1e2a-164">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="a1e2a-164">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="a1e2a-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1e2a-165">NOTES</span></span>

## <span data-ttu-id="a1e2a-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1e2a-166">RELATED LINKS</span></span>

[<span data-ttu-id="a1e2a-167">Yedek-azurermapı</span><span class="sxs-lookup"><span data-stu-id="a1e2a-167">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="a1e2a-168">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="a1e2a-168">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="a1e2a-169">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="a1e2a-169">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="a1e2a-170">Geri yükleme-azurermapı</span><span class="sxs-lookup"><span data-stu-id="a1e2a-170">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


