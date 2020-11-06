---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 82e09e146999ce0bd320ba398ab2f196f1115688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591243"
---
# <span data-ttu-id="07afa-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="07afa-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="07afa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07afa-102">SYNOPSIS</span></span>
<span data-ttu-id="07afa-103">Bir API yönetim dağıtımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07afa-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07afa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07afa-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07afa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07afa-105">DESCRIPTION</span></span>
<span data-ttu-id="07afa-106">**Yeni-Azurermapsanana,** Azure API YÖNETIMINDE bir API yönetim dağıtımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07afa-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="07afa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07afa-107">EXAMPLES</span></span>

### <span data-ttu-id="07afa-108">Örnek 1: Geliştirici katmanı API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="07afa-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="07afa-109">Bu komut bir geliştirici katmanı API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07afa-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="07afa-110">Bu komut, organizasyonu ve yönetici adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07afa-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="07afa-111">Komut *SKU* parametresini belirtmez.</span><span class="sxs-lookup"><span data-stu-id="07afa-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="07afa-112">Bu nedenle, cmdlet geliştirici varsayılan değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="07afa-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="07afa-113">Örnek 2: üç birimli standart bir katman hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="07afa-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="07afa-114">Bu komut, üç birimli bir standart katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07afa-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="07afa-115">Örnek 3: dış sanal ağ için API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="07afa-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="07afa-116">Bu komut, bir Azure sanal ağ alt ağında, Batı ABD 'deki ana bölgeyle birlikte dış bir ağ geçidi uç noktası içeren bir Premium katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07afa-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="07afa-117">Örnek 4: iç sanal ağ için bir API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="07afa-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="07afa-118">Bu komut, bir Azure sanal ağ alt ağında, Batı ABD 'deki ana bölgeyle birlikte dahili bir ağ geçidi uç noktası içeren bir Premium katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07afa-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="07afa-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07afa-119">PARAMETERS</span></span>

### <span data-ttu-id="07afa-120">-Additionalbölgelerle</span><span class="sxs-lookup"><span data-stu-id="07afa-120">-AdditionalRegions</span></span>
<span data-ttu-id="07afa-121">Azure API yönetimi için ek dağıtım bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="07afa-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07afa-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="07afa-122">-AdminEmail</span></span>
<span data-ttu-id="07afa-123">API yönetim sisteminin gönderdiği tüm bildirimler için kaynak e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07afa-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="07afa-124">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="07afa-124">-Capacity</span></span>
<span data-ttu-id="07afa-125">Azure API yönetim hizmetinin SKU kapasitesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07afa-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="07afa-126">Varsayılan değer bir (1).</span><span class="sxs-lookup"><span data-stu-id="07afa-126">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07afa-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="07afa-127">-Location</span></span>
<span data-ttu-id="07afa-128">Bu cmdlet 'in API yönetim dağıtımını oluşturduğu konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07afa-128">Specifies the location in which this cmdlet creates an API Management deployment.</span></span>
<span data-ttu-id="07afa-129">Geçerli konumları almak için Get-AzureLocation cmdlet 'lerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="07afa-129">To obtain valid locations, use the Get-AzureLocation cmdlets.</span></span>

<span data-ttu-id="07afa-130">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="07afa-130">Valid values are:</span></span> 

- <span data-ttu-id="07afa-131">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="07afa-131">North Central US</span></span>
- <span data-ttu-id="07afa-132">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="07afa-132">South Central US</span></span>
- <span data-ttu-id="07afa-133">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="07afa-133">Central US</span></span>
- <span data-ttu-id="07afa-134">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="07afa-134">West Europe</span></span>
- <span data-ttu-id="07afa-135">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="07afa-135">North Europe</span></span>
- <span data-ttu-id="07afa-136">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="07afa-136">West US</span></span>
- <span data-ttu-id="07afa-137">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="07afa-137">East US</span></span>
- <span data-ttu-id="07afa-138">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="07afa-138">East US 2</span></span>
- <span data-ttu-id="07afa-139">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="07afa-139">Japan East</span></span>
- <span data-ttu-id="07afa-140">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="07afa-140">Japan West</span></span>
- <span data-ttu-id="07afa-141">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="07afa-141">Brazil South</span></span>
- <span data-ttu-id="07afa-142">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="07afa-142">Southeast Asia</span></span>
- <span data-ttu-id="07afa-143">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="07afa-143">East Asia</span></span>
- <span data-ttu-id="07afa-144">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="07afa-144">Australia East</span></span>
- <span data-ttu-id="07afa-145">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="07afa-145">Australia Southeast</span></span>

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

### <span data-ttu-id="07afa-146">-Ad</span><span class="sxs-lookup"><span data-stu-id="07afa-146">-Name</span></span>
<span data-ttu-id="07afa-147">API yönetim dağıtımı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="07afa-147">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="07afa-148">-Kuruluş</span><span class="sxs-lookup"><span data-stu-id="07afa-148">-Organization</span></span>
<span data-ttu-id="07afa-149">Kuruluşun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07afa-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="07afa-150">API Yönetimi, bu adresi Geliştirici Portalında e-posta bildirimlerinde kullanır.</span><span class="sxs-lookup"><span data-stu-id="07afa-150">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="07afa-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07afa-151">-ResourceGroupName</span></span>
<span data-ttu-id="07afa-152">Bu cmdlet 'in API yönetim dağıtımını oluşturduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07afa-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="07afa-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="07afa-153">-Sku</span></span>
<span data-ttu-id="07afa-154">API yönetim hizmetinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07afa-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="07afa-155">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="07afa-155">Valid values are:</span></span> 

- <span data-ttu-id="07afa-156">İyle</span><span class="sxs-lookup"><span data-stu-id="07afa-156">Developer</span></span> 
- <span data-ttu-id="07afa-157">Ardından</span><span class="sxs-lookup"><span data-stu-id="07afa-157">Standard</span></span> 
- <span data-ttu-id="07afa-158">Min</span><span class="sxs-lookup"><span data-stu-id="07afa-158">Premium</span></span> 

<span data-ttu-id="07afa-159">Varsayılan olarak geliştirici kullanılır.</span><span class="sxs-lookup"><span data-stu-id="07afa-159">The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07afa-160">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="07afa-160">-Tags</span></span>
<span data-ttu-id="07afa-161">Etiketlerin sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="07afa-161">Specifies a dictionary of tags.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07afa-162">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="07afa-162">-VirtualNetwork</span></span>
<span data-ttu-id="07afa-163">Master Azure API yönetim dağıtım bölgesinin sanal ağ yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="07afa-163">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07afa-164">-VpnType</span><span class="sxs-lookup"><span data-stu-id="07afa-164">-VpnType</span></span>
<span data-ttu-id="07afa-165">Sanal ağ 'ın sanal ağ türü.</span><span class="sxs-lookup"><span data-stu-id="07afa-165">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="07afa-166">Geçerli değerler</span><span class="sxs-lookup"><span data-stu-id="07afa-166">Valid Values are</span></span> 
- <span data-ttu-id="07afa-167">"None" (varsayılan değer.</span><span class="sxs-lookup"><span data-stu-id="07afa-167">"None" (Default Value.</span></span> <span data-ttu-id="07afa-168">Herhangi bir sanal ağın parçası değildir ")</span><span class="sxs-lookup"><span data-stu-id="07afa-168">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="07afa-169">"Dış" (bir Internet 'e yönelik uç noktaya sahip bir sanal ağın içinde bir kuruluş)</span><span class="sxs-lookup"><span data-stu-id="07afa-169">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="07afa-170">"İç" (bir sanal ağın iç uç noktasına sahip olduğu bir sanal ağ içinde, kuruluş)</span><span class="sxs-lookup"><span data-stu-id="07afa-170">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07afa-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07afa-171">-DefaultProfile</span></span>
<span data-ttu-id="07afa-172">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07afa-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07afa-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07afa-173">CommonParameters</span></span>
<span data-ttu-id="07afa-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07afa-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07afa-175">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07afa-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07afa-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07afa-176">INPUTS</span></span>

## <span data-ttu-id="07afa-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07afa-177">OUTPUTS</span></span>

### <span data-ttu-id="07afa-178">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="07afa-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="07afa-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07afa-179">NOTES</span></span>

## <span data-ttu-id="07afa-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07afa-180">RELATED LINKS</span></span>

[<span data-ttu-id="07afa-181">Yedek-azurermapı</span><span class="sxs-lookup"><span data-stu-id="07afa-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="07afa-182">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="07afa-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="07afa-183">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="07afa-183">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="07afa-184">Geri yükleme-azurermapı</span><span class="sxs-lookup"><span data-stu-id="07afa-184">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


