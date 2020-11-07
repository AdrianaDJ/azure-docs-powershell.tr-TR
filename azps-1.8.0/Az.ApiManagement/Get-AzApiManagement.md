---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: c636da952c02b4f2b4795cd1703c276a23a8221c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751180"
---
# <span data-ttu-id="8907a-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="8907a-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="8907a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8907a-102">SYNOPSIS</span></span>
<span data-ttu-id="8907a-103">Bir listeyi veya belirli bir API yönetim hizmeti açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="8907a-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="8907a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8907a-104">SYNTAX</span></span>

### <span data-ttu-id="8907a-105">GetBySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8907a-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8907a-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8907a-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8907a-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="8907a-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8907a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8907a-108">DESCRIPTION</span></span>
<span data-ttu-id="8907a-109">**Get-Azapsananaveya** belırlı bir API Yönetimi altındakı tüm API yönetim hizmetlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="8907a-109">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="8907a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8907a-110">EXAMPLES</span></span>

### <span data-ttu-id="8907a-111">Örnek 1: tüm API yönetim hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="8907a-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="8907a-112">Bu komut, bir aboneliğin içindeki tüm API yönetim hizmetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8907a-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="8907a-113">Örnek 2: belirli bir ad ile tüm API yönetim hizmetlerini alma</span><span class="sxs-lookup"><span data-stu-id="8907a-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="8907a-114">Bu komut tüm API yönetim hizmetlerini adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="8907a-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="8907a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8907a-115">PARAMETERS</span></span>

### <span data-ttu-id="8907a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8907a-116">-DefaultProfile</span></span>
<span data-ttu-id="8907a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8907a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8907a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="8907a-118">-Name</span></span>
<span data-ttu-id="8907a-119">API yönetim hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8907a-119">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="8907a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8907a-120">-ResourceGroupName</span></span>
<span data-ttu-id="8907a-121">Bu cmdlet 'in API Yönetim hizmetini aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8907a-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="8907a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8907a-122">CommonParameters</span></span>
<span data-ttu-id="8907a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8907a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8907a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8907a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8907a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8907a-125">INPUTS</span></span>

### <span data-ttu-id="8907a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8907a-126">System.String</span></span>

## <span data-ttu-id="8907a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8907a-127">OUTPUTS</span></span>

### <span data-ttu-id="8907a-128">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="8907a-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="8907a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8907a-129">NOTES</span></span>

## <span data-ttu-id="8907a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8907a-130">RELATED LINKS</span></span>

[<span data-ttu-id="8907a-131">Yedek-azlı bir</span><span class="sxs-lookup"><span data-stu-id="8907a-131">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="8907a-132">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="8907a-132">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="8907a-133">Remove-azın</span><span class="sxs-lookup"><span data-stu-id="8907a-133">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="8907a-134">Geri yükleme-azbir</span><span class="sxs-lookup"><span data-stu-id="8907a-134">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


