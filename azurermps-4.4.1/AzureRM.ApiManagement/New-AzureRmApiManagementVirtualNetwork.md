---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587038"
---
# <span data-ttu-id="12d78-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="12d78-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="12d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12d78-102">SYNOPSIS</span></span>
<span data-ttu-id="12d78-103">PsApiManagementVirtualNetwork örneğini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12d78-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12d78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12d78-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12d78-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12d78-105">DESCRIPTION</span></span>
<span data-ttu-id="12d78-106">**New-AzureRmApiManagementVirtualNetwork** cmdlet 'i, bir **PsApiManagementVirtualNetwork** örneği oluşturmak için yardımcı komuttur.</span><span class="sxs-lookup"><span data-stu-id="12d78-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="12d78-107">Bu komut **set-Azurermapımanagementvirtualnetworks** cmdlet ile kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12d78-107">This command is used with **Set-AzureRMApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="12d78-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12d78-108">EXAMPLES</span></span>

### <span data-ttu-id="12d78-109">Örnek 1: sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="12d78-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

<span data-ttu-id="12d78-110">Bu örnekte sanal bir ağ oluşturulur ve ardından **set-Azurermapımanagementvirtualnetworks** cmdlet 'ini arar.</span><span class="sxs-lookup"><span data-stu-id="12d78-110">This example creates a virtual network and then calls the **Set-AzureRmApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="12d78-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12d78-111">PARAMETERS</span></span>

### <span data-ttu-id="12d78-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="12d78-112">-Location</span></span>
<span data-ttu-id="12d78-113">Bu cmdlet 'in örneği oluşturduğu sanal ağın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="12d78-113">Specifies the location of the virtual network in which this cmdlet creates the instance.</span></span>

<span data-ttu-id="12d78-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="12d78-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="12d78-115">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="12d78-115">North Central US</span></span>
- <span data-ttu-id="12d78-116">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="12d78-116">South Central US</span></span>
- <span data-ttu-id="12d78-117">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="12d78-117">Central US</span></span>
- <span data-ttu-id="12d78-118">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="12d78-118">West Europe</span></span>
- <span data-ttu-id="12d78-119">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="12d78-119">North Europe</span></span>
- <span data-ttu-id="12d78-120">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="12d78-120">West US</span></span>
- <span data-ttu-id="12d78-121">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="12d78-121">East US</span></span>
- <span data-ttu-id="12d78-122">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="12d78-122">East US 2</span></span>
- <span data-ttu-id="12d78-123">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="12d78-123">Japan East</span></span>
- <span data-ttu-id="12d78-124">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="12d78-124">Japan West</span></span>
- <span data-ttu-id="12d78-125">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="12d78-125">Brazil South</span></span>
- <span data-ttu-id="12d78-126">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="12d78-126">Southeast Asia</span></span>
- <span data-ttu-id="12d78-127">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="12d78-127">East Asia</span></span>
- <span data-ttu-id="12d78-128">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="12d78-128">Australia East</span></span>
- <span data-ttu-id="12d78-129">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="12d78-129">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d78-130">-Subnetresourceıd</span><span class="sxs-lookup"><span data-stu-id="12d78-130">-SubnetResourceId</span></span>
<span data-ttu-id="12d78-131">Sanal ağın alt ağ kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="12d78-131">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d78-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d78-132">-DefaultProfile</span></span>
<span data-ttu-id="12d78-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12d78-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12d78-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d78-134">CommonParameters</span></span>
<span data-ttu-id="12d78-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12d78-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d78-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d78-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d78-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12d78-137">INPUTS</span></span>

## <span data-ttu-id="12d78-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12d78-138">OUTPUTS</span></span>

### <span data-ttu-id="12d78-139">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="12d78-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="12d78-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12d78-140">NOTES</span></span>

## <span data-ttu-id="12d78-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12d78-141">RELATED LINKS</span></span>

