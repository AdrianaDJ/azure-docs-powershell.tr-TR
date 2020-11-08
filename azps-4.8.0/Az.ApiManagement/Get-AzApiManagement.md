---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274216"
---
# <span data-ttu-id="7f300-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="7f300-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="7f300-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f300-102">SYNOPSIS</span></span>
<span data-ttu-id="7f300-103">Bir listeyi veya belirli bir API yönetim hizmeti açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="7f300-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="7f300-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f300-104">SYNTAX</span></span>

### <span data-ttu-id="7f300-105">GetBySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f300-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f300-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7f300-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f300-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="7f300-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f300-108">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="7f300-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f300-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f300-109">DESCRIPTION</span></span>
<span data-ttu-id="7f300-110">**Get-Azapsananaveya** belırlı bir API Yönetimi altındakı tüm API yönetim hizmetlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="7f300-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="7f300-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f300-111">EXAMPLES</span></span>

### <span data-ttu-id="7f300-112">Örnek 1: tüm API yönetim hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="7f300-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="7f300-113">Bu komut, bir aboneliğin içindeki tüm API yönetim hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="7f300-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="7f300-114">Örnek 2: belirli bir ad ile tüm API yönetim hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="7f300-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="7f300-115">Bu komut tüm API yönetim hizmetlerini adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="7f300-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="7f300-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f300-116">PARAMETERS</span></span>

### <span data-ttu-id="7f300-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f300-117">-DefaultProfile</span></span>
<span data-ttu-id="7f300-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f300-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f300-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f300-119">-Name</span></span>
<span data-ttu-id="7f300-120">API yönetim hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f300-120">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f300-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f300-121">-ResourceGroupName</span></span>
<span data-ttu-id="7f300-122">Bu cmdlet 'in API Yönetim hizmetini aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f300-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f300-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7f300-123">-ResourceId</span></span>
<span data-ttu-id="7f300-124">API yönetim hizmetinin ARM RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="7f300-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f300-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f300-125">CommonParameters</span></span>
<span data-ttu-id="7f300-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f300-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f300-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7f300-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f300-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f300-128">INPUTS</span></span>

### <span data-ttu-id="7f300-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7f300-129">System.String</span></span>

## <span data-ttu-id="7f300-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f300-130">OUTPUTS</span></span>

### <span data-ttu-id="7f300-131">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="7f300-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="7f300-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f300-132">NOTES</span></span>

## <span data-ttu-id="7f300-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f300-133">RELATED LINKS</span></span>

[<span data-ttu-id="7f300-134">Yedek-azlı bir</span><span class="sxs-lookup"><span data-stu-id="7f300-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="7f300-135">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="7f300-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="7f300-136">Remove-azın</span><span class="sxs-lookup"><span data-stu-id="7f300-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="7f300-137">Geri yükleme-azbir</span><span class="sxs-lookup"><span data-stu-id="7f300-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


