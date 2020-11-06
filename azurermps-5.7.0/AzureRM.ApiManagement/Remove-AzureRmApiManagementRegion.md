---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 0376c80e769153c448cdc23d8465966026584fcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595129"
---
# <span data-ttu-id="73027-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="73027-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="73027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73027-102">SYNOPSIS</span></span>
<span data-ttu-id="73027-103">Psapsananaddeğerinden var olan bir dağıtım bölgesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73027-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73027-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73027-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73027-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="73027-105">DESCRIPTION</span></span>
<span data-ttu-id="73027-106">**Remove-Azurermapsananagementregion** cmdlet 'i, Microsoft. Azure. Commands. **Apsananad. model. psapsananad,** sağlanan bir **Additionalregion** koleksiyonundan **Microsoft. Azure. Commands**</span><span class="sxs-lookup"><span data-stu-id="73027-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="73027-107">Bu cmdlet, dağıtımı kendi başına değiştirmez ancak bellekteki **Psapımana**</span><span class="sxs-lookup"><span data-stu-id="73027-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="73027-108">Bir API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapsananagementınstance** öğesini **güncelleştirmeye-Azurermapsananae** geçirin.</span><span class="sxs-lookup"><span data-stu-id="73027-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="73027-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73027-109">EXAMPLES</span></span>

### <span data-ttu-id="73027-110">Örnek 1: psapsanana</span><span class="sxs-lookup"><span data-stu-id="73027-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="73027-111">Bu komut, **Psapsananadus** ÖRNEĞINDEKI Doğu US adındaki bölgeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73027-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="73027-112">Örnek 2: bir dizi komutu kullanarak psapsanana</span><span class="sxs-lookup"><span data-stu-id="73027-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="73027-113">İlk komut, contoso adlı bir kaynak grubundan Contosoapı adlı kaynak grubundan bir **Psapsananadörneği** alır.</span><span class="sxs-lookup"><span data-stu-id="73027-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="73027-114">Son komutu daha sonra o örnekten Doğu ABD adlı bölgeyi kaldırır ve dağıtımı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="73027-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="73027-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73027-115">PARAMETERS</span></span>

### <span data-ttu-id="73027-116">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="73027-116">-ApiManagement</span></span>
<span data-ttu-id="73027-117">Bu cmdlet 'in ek dağıtım bölgesini kaldırdığı **Psapimanadörneği** 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="73027-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73027-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73027-118">-DefaultProfile</span></span>
<span data-ttu-id="73027-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73027-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="73027-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="73027-120">-Location</span></span>
<span data-ttu-id="73027-121">Bu cmdlet 'in kaldırıldığı bölgenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="73027-121">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="73027-122">API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="73027-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="73027-123">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="73027-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="73027-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73027-124">CommonParameters</span></span>
<span data-ttu-id="73027-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73027-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73027-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73027-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73027-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73027-127">INPUTS</span></span>

### <span data-ttu-id="73027-128">Bağış</span><span class="sxs-lookup"><span data-stu-id="73027-128">PsApiManagement</span></span>
<span data-ttu-id="73027-129">Parametre ' Apsananadeğeri ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="73027-129">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="73027-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73027-130">OUTPUTS</span></span>

### <span data-ttu-id="73027-131">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="73027-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="73027-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73027-132">NOTES</span></span>

## <span data-ttu-id="73027-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73027-133">RELATED LINKS</span></span>

[<span data-ttu-id="73027-134">Add-Azurermapımanagementregion</span><span class="sxs-lookup"><span data-stu-id="73027-134">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="73027-135">Güncelleştirme-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="73027-135">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


