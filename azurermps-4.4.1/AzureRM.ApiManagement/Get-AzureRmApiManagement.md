---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 610f8589dbb6c01cae1a3eb37f886425a3664929
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587048"
---
# <span data-ttu-id="0865d-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0865d-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="0865d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0865d-102">SYNOPSIS</span></span>
<span data-ttu-id="0865d-103">Bir listeyi veya belirli bir API yönetim hizmeti açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="0865d-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0865d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0865d-104">SYNTAX</span></span>

### <span data-ttu-id="0865d-105">Tüm abonelikte (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0865d-105">All In Subscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0865d-106">Tümü kaynak grubunda</span><span class="sxs-lookup"><span data-stu-id="0865d-106">All In Resource Group</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0865d-107">Belirli API Yönetimi hizmeti</span><span class="sxs-lookup"><span data-stu-id="0865d-107">Specific API Management Service</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0865d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0865d-108">DESCRIPTION</span></span>
<span data-ttu-id="0865d-109">**Get-Azurermapsananaks** cmdlet 'i, aboneliğin veya BELIRTILEN bir API yönetiminin altındakı tüm API yönetim hizmetlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="0865d-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="0865d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0865d-110">EXAMPLES</span></span>

### <span data-ttu-id="0865d-111">Örnek 1: tüm API yönetim hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="0865d-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="0865d-112">Bu komut, bir aboneliğin içindeki tüm API yönetim hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0865d-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="0865d-113">Örnek 2: belirli bir ad ile tüm API yönetim hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="0865d-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="0865d-114">Bu komut tüm API yönetim hizmetlerini adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="0865d-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="0865d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0865d-115">PARAMETERS</span></span>

### <span data-ttu-id="0865d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0865d-116">-Name</span></span>
<span data-ttu-id="0865d-117">API yönetim hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0865d-117">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0865d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0865d-118">-ResourceGroupName</span></span>
<span data-ttu-id="0865d-119">Bu cmdlet 'in API Yönetim hizmetini aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0865d-119">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0865d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0865d-120">-DefaultProfile</span></span>
<span data-ttu-id="0865d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0865d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0865d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0865d-122">CommonParameters</span></span>
<span data-ttu-id="0865d-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0865d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0865d-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0865d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0865d-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0865d-125">INPUTS</span></span>

## <span data-ttu-id="0865d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0865d-126">OUTPUTS</span></span>

### <span data-ttu-id="0865d-127">System. Koleksiyonlar. Generic. List ' 1 [Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="0865d-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="0865d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0865d-128">NOTES</span></span>

## <span data-ttu-id="0865d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0865d-129">RELATED LINKS</span></span>

[<span data-ttu-id="0865d-130">Yedek-azurermapı</span><span class="sxs-lookup"><span data-stu-id="0865d-130">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="0865d-131">Yeni-azurermapı</span><span class="sxs-lookup"><span data-stu-id="0865d-131">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="0865d-132">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="0865d-132">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="0865d-133">Geri yükleme-azurermapı</span><span class="sxs-lookup"><span data-stu-id="0865d-133">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


