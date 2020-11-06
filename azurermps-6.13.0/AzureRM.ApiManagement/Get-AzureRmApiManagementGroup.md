---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: d18de5494912900be4a73414e8741badb097d188
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592356"
---
# <span data-ttu-id="6eec9-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6eec9-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="6eec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eec9-102">SYNOPSIS</span></span>
<span data-ttu-id="6eec9-103">Tüm veya belirli API Yönetim gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="6eec9-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eec9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6eec9-104">SYNTAX</span></span>

### <span data-ttu-id="6eec9-105">GetAllGroups (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6eec9-105">GetAllGroups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eec9-106">Getbygroupıd</span><span class="sxs-lookup"><span data-stu-id="6eec9-106">GetByGroupId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eec9-107">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="6eec9-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eec9-108">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="6eec9-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eec9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6eec9-109">DESCRIPTION</span></span>
<span data-ttu-id="6eec9-110">**Get-Azurermapımanagementgroup** cmdlet 'i veya belirli API Yönetim gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="6eec9-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="6eec9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6eec9-111">EXAMPLES</span></span>

### <span data-ttu-id="6eec9-112">Örnek 1: tüm grupları Al</span><span class="sxs-lookup"><span data-stu-id="6eec9-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext
```

<span data-ttu-id="6eec9-113">Bu komut tüm grupları alır.</span><span class="sxs-lookup"><span data-stu-id="6eec9-113">This command gets all groups.</span></span>

### <span data-ttu-id="6eec9-114">Örnek 2: bir grup KIMLIĞI alma</span><span class="sxs-lookup"><span data-stu-id="6eec9-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="6eec9-115">Bu komut, 0123456789 adlı grup KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="6eec9-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="6eec9-116">Örnek 3: ada göre grupla</span><span class="sxs-lookup"><span data-stu-id="6eec9-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="6eec9-117">Bu komut, Group0002 adlı grubu alır.</span><span class="sxs-lookup"><span data-stu-id="6eec9-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="6eec9-118">Örnek 4: tüm Kullanıcı gruplarını alma</span><span class="sxs-lookup"><span data-stu-id="6eec9-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="6eec9-119">Bu komut, 0123456789 adlı Kullanıcı KIMLIĞINE sahip tüm Kullanıcı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="6eec9-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="6eec9-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6eec9-120">PARAMETERS</span></span>

### <span data-ttu-id="6eec9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="6eec9-121">-Context</span></span>
<span data-ttu-id="6eec9-122">Psapsananagementcontext örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eec9-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eec9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eec9-123">-DefaultProfile</span></span>
<span data-ttu-id="6eec9-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6eec9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eec9-125">-GroupID</span><span class="sxs-lookup"><span data-stu-id="6eec9-125">-GroupId</span></span>
<span data-ttu-id="6eec9-126">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eec9-126">Specifies the group ID.</span></span>
<span data-ttu-id="6eec9-127">Belirtilmişse, cmdlet tanıtıcıyı tanımlayıcı tarafından bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="6eec9-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="6eec9-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="6eec9-128">-Name</span></span>
<span data-ttu-id="6eec9-129">Yönetim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eec9-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="6eec9-130">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="6eec9-130">-ProductId</span></span>
<span data-ttu-id="6eec9-131">Var olan ürünün tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6eec9-131">Identifier of existing product.</span></span>
<span data-ttu-id="6eec9-132">Belirtilirse, ürünün atandığı tüm grupları döndürür.</span><span class="sxs-lookup"><span data-stu-id="6eec9-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="6eec9-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6eec9-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="6eec9-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="6eec9-134">-UserId</span></span>
<span data-ttu-id="6eec9-135">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6eec9-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="6eec9-136">Belirtilmişse cmdlet, ürünün atandığı tüm grupları döndürür.</span><span class="sxs-lookup"><span data-stu-id="6eec9-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="6eec9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eec9-137">CommonParameters</span></span>
<span data-ttu-id="6eec9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6eec9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eec9-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eec9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eec9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6eec9-140">INPUTS</span></span>

### <span data-ttu-id="6eec9-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6eec9-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6eec9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6eec9-142">System.String</span></span>

## <span data-ttu-id="6eec9-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6eec9-143">OUTPUTS</span></span>

### <span data-ttu-id="6eec9-144">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="6eec9-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="6eec9-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6eec9-145">NOTES</span></span>

## <span data-ttu-id="6eec9-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6eec9-146">RELATED LINKS</span></span>

[<span data-ttu-id="6eec9-147">Yeni-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="6eec9-147">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="6eec9-148">Remove-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="6eec9-148">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="6eec9-149">Set-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="6eec9-149">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


