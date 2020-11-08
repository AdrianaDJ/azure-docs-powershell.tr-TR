---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273767"
---
# <span data-ttu-id="46e9e-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="46e9e-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="46e9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="46e9e-103">Tüm veya belirli API Yönetim gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="46e9e-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="46e9e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46e9e-104">SYNTAX</span></span>

### <span data-ttu-id="46e9e-105">GetAllGroups (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="46e9e-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e9e-106">Getbygroupıd</span><span class="sxs-lookup"><span data-stu-id="46e9e-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e9e-107">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="46e9e-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e9e-108">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="46e9e-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46e9e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="46e9e-109">DESCRIPTION</span></span>
<span data-ttu-id="46e9e-110">**Get-Azapsananagementgroup** cmdlet 'i ya da belirli API Yönetim gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="46e9e-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="46e9e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46e9e-111">EXAMPLES</span></span>

### <span data-ttu-id="46e9e-112">Örnek 1: tüm grupları Al</span><span class="sxs-lookup"><span data-stu-id="46e9e-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="46e9e-113">Bu komut tüm grupları alır.</span><span class="sxs-lookup"><span data-stu-id="46e9e-113">This command gets all groups.</span></span>

### <span data-ttu-id="46e9e-114">Örnek 2: bir grup KIMLIĞI alma</span><span class="sxs-lookup"><span data-stu-id="46e9e-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="46e9e-115">Bu komut, 0123456789 adlı grup KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="46e9e-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="46e9e-116">Örnek 3: ada göre grupla</span><span class="sxs-lookup"><span data-stu-id="46e9e-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="46e9e-117">Bu komut, Group0002 adlı grubu alır.</span><span class="sxs-lookup"><span data-stu-id="46e9e-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="46e9e-118">Örnek 4: tüm Kullanıcı gruplarını alma</span><span class="sxs-lookup"><span data-stu-id="46e9e-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="46e9e-119">Bu komut, 0123456789 adlı Kullanıcı KIMLIĞINE sahip tüm Kullanıcı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="46e9e-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="46e9e-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46e9e-120">PARAMETERS</span></span>

### <span data-ttu-id="46e9e-121">-Context</span><span class="sxs-lookup"><span data-stu-id="46e9e-121">-Context</span></span>
<span data-ttu-id="46e9e-122">Psapsananagementcontext örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46e9e-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46e9e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e9e-123">-DefaultProfile</span></span>
<span data-ttu-id="46e9e-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46e9e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46e9e-125">-GroupID</span><span class="sxs-lookup"><span data-stu-id="46e9e-125">-GroupId</span></span>
<span data-ttu-id="46e9e-126">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="46e9e-126">Specifies the group ID.</span></span>
<span data-ttu-id="46e9e-127">Belirtilmişse, cmdlet tanıtıcıyı tanımlayıcı tarafından bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="46e9e-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e9e-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="46e9e-128">-Name</span></span>
<span data-ttu-id="46e9e-129">Yönetim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46e9e-129">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e9e-130">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="46e9e-130">-ProductId</span></span>
<span data-ttu-id="46e9e-131">Var olan ürünün tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="46e9e-131">Identifier of existing product.</span></span>
<span data-ttu-id="46e9e-132">Belirtilirse, ürünün atandığı tüm grupları döndürür.</span><span class="sxs-lookup"><span data-stu-id="46e9e-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="46e9e-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="46e9e-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e9e-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="46e9e-134">-UserId</span></span>
<span data-ttu-id="46e9e-135">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46e9e-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="46e9e-136">Belirtilmişse cmdlet, ürünün atandığı tüm grupları döndürür.</span><span class="sxs-lookup"><span data-stu-id="46e9e-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e9e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e9e-137">CommonParameters</span></span>
<span data-ttu-id="46e9e-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46e9e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e9e-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="46e9e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e9e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46e9e-140">INPUTS</span></span>

### <span data-ttu-id="46e9e-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="46e9e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="46e9e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="46e9e-142">System.String</span></span>

## <span data-ttu-id="46e9e-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46e9e-143">OUTPUTS</span></span>

### <span data-ttu-id="46e9e-144">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="46e9e-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="46e9e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46e9e-145">NOTES</span></span>

## <span data-ttu-id="46e9e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46e9e-146">RELATED LINKS</span></span>

[<span data-ttu-id="46e9e-147">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="46e9e-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="46e9e-148">Remove-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="46e9e-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="46e9e-149">Set-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="46e9e-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


