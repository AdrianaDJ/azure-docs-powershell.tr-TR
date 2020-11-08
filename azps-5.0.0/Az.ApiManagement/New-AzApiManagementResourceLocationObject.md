---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277094"
---
# <span data-ttu-id="40ca6-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="40ca6-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="40ca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="40ca6-103">Yeni bir kaynak konumu sözleşmesi oluşturun (ağ geçitlerinde kullanılır).</span><span class="sxs-lookup"><span data-stu-id="40ca6-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="40ca6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40ca6-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40ca6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40ca6-105">DESCRIPTION</span></span>
<span data-ttu-id="40ca6-106">**Yeni-Azapsananagementresourseocationobject** cmdlet 'i, yeni bir kaynak konumu Sözleşmesi (ağ geçitlerinde kullanılır) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40ca6-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="40ca6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40ca6-107">EXAMPLES</span></span>

### <span data-ttu-id="40ca6-108">Örnek 1: kaynak konumu sözleşmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="40ca6-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="40ca6-109">Bu komut bir kaynak konumu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40ca6-109">This command creates a resource location.</span></span>

## <span data-ttu-id="40ca6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40ca6-110">PARAMETERS</span></span>

### <span data-ttu-id="40ca6-111">-Şehir</span><span class="sxs-lookup"><span data-stu-id="40ca6-111">-City</span></span>
<span data-ttu-id="40ca6-112">Konum şehri.</span><span class="sxs-lookup"><span data-stu-id="40ca6-112">Location City.</span></span>
<span data-ttu-id="40ca6-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="40ca6-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="40ca6-114">-CountryOrRegion</span></span>
<span data-ttu-id="40ca6-115">Ülke veya bölge.</span><span class="sxs-lookup"><span data-stu-id="40ca6-115">Location Country or Region.</span></span>
<span data-ttu-id="40ca6-116">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="40ca6-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ca6-117">-DefaultProfile</span></span>
<span data-ttu-id="40ca6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40ca6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40ca6-119">-District</span><span class="sxs-lookup"><span data-stu-id="40ca6-119">-District</span></span>
<span data-ttu-id="40ca6-120">Konum bölgesi.</span><span class="sxs-lookup"><span data-stu-id="40ca6-120">Location District.</span></span>
<span data-ttu-id="40ca6-121">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="40ca6-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="40ca6-122">-Name</span></span>
<span data-ttu-id="40ca6-123">Konum adı.</span><span class="sxs-lookup"><span data-stu-id="40ca6-123">Location Name.</span></span>
<span data-ttu-id="40ca6-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="40ca6-124">This parameter is required.</span></span>

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

### <span data-ttu-id="40ca6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ca6-125">CommonParameters</span></span>
<span data-ttu-id="40ca6-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40ca6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ca6-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="40ca6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ca6-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40ca6-128">INPUTS</span></span>

### <span data-ttu-id="40ca6-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="40ca6-129">None</span></span>

## <span data-ttu-id="40ca6-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40ca6-130">OUTPUTS</span></span>

### <span data-ttu-id="40ca6-131">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementresourcelocation</span><span class="sxs-lookup"><span data-stu-id="40ca6-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="40ca6-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40ca6-132">NOTES</span></span>

## <span data-ttu-id="40ca6-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40ca6-133">RELATED LINKS</span></span>
