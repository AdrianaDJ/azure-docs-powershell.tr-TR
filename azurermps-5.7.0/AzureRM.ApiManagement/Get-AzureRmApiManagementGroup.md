---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: b77452bff93a9b66f8ffe54fdff623d391749622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592516"
---
# <span data-ttu-id="d49c8-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d49c8-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="d49c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d49c8-102">SYNOPSIS</span></span>
<span data-ttu-id="d49c8-103">Tüm veya belirli API Yönetim gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d49c8-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d49c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d49c8-104">SYNTAX</span></span>

### <span data-ttu-id="d49c8-105">GetAllGroups (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d49c8-105">GetAllGroups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d49c8-106">Getbygroupıd</span><span class="sxs-lookup"><span data-stu-id="d49c8-106">GetByGroupId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d49c8-107">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="d49c8-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d49c8-108">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="d49c8-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d49c8-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d49c8-109">DESCRIPTION</span></span>
<span data-ttu-id="d49c8-110">**Get-Azurermapımanagementgroup** cmdlet 'i veya belirli API Yönetim gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d49c8-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="d49c8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d49c8-111">EXAMPLES</span></span>

### <span data-ttu-id="d49c8-112">Örnek 1: tüm grupları Al</span><span class="sxs-lookup"><span data-stu-id="d49c8-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext
```

<span data-ttu-id="d49c8-113">Bu komut tüm grupları alır.</span><span class="sxs-lookup"><span data-stu-id="d49c8-113">This command gets all groups.</span></span>

### <span data-ttu-id="d49c8-114">Örnek 2: bir grup KIMLIĞI alma</span><span class="sxs-lookup"><span data-stu-id="d49c8-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="d49c8-115">Bu komut, 0123456789 adlı grup KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="d49c8-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="d49c8-116">Örnek 3: ada göre grupla</span><span class="sxs-lookup"><span data-stu-id="d49c8-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="d49c8-117">Bu komut, Group0002 adlı grubu alır.</span><span class="sxs-lookup"><span data-stu-id="d49c8-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="d49c8-118">Örnek 4: tüm Kullanıcı gruplarını alma</span><span class="sxs-lookup"><span data-stu-id="d49c8-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="d49c8-119">Bu komut, 0123456789 adlı Kullanıcı KIMLIĞINE sahip tüm Kullanıcı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="d49c8-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="d49c8-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d49c8-120">PARAMETERS</span></span>

### <span data-ttu-id="d49c8-121">-Context</span><span class="sxs-lookup"><span data-stu-id="d49c8-121">-Context</span></span>
<span data-ttu-id="d49c8-122">Psapsananagementcontext örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d49c8-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49c8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49c8-123">-DefaultProfile</span></span>
<span data-ttu-id="d49c8-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d49c8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d49c8-125">-GroupID</span><span class="sxs-lookup"><span data-stu-id="d49c8-125">-GroupId</span></span>
<span data-ttu-id="d49c8-126">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d49c8-126">Specifies the group ID.</span></span>
<span data-ttu-id="d49c8-127">Belirtilmişse, cmdlet tanıtıcıyı tanımlayıcı tarafından bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="d49c8-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByGroupId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49c8-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="d49c8-128">-Name</span></span>
<span data-ttu-id="d49c8-129">Yönetim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d49c8-129">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49c8-130">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="d49c8-130">-ProductId</span></span>
<span data-ttu-id="d49c8-131">Var olan ürünün tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="d49c8-131">Identifier of existing product.</span></span>
<span data-ttu-id="d49c8-132">Belirtilirse, ürünün atandığı tüm grupları döndürür.</span><span class="sxs-lookup"><span data-stu-id="d49c8-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="d49c8-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d49c8-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49c8-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="d49c8-134">-UserId</span></span>
<span data-ttu-id="d49c8-135">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d49c8-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="d49c8-136">Belirtilmişse cmdlet, ürünün atandığı tüm grupları döndürür.</span><span class="sxs-lookup"><span data-stu-id="d49c8-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49c8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49c8-137">CommonParameters</span></span>
<span data-ttu-id="d49c8-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d49c8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49c8-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d49c8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49c8-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d49c8-140">INPUTS</span></span>

### <span data-ttu-id="d49c8-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d49c8-141">None</span></span>
<span data-ttu-id="d49c8-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d49c8-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d49c8-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d49c8-143">OUTPUTS</span></span>

### <span data-ttu-id="d49c8-144">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="d49c8-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>
<span data-ttu-id="d49c8-145">API Yönetimi hizmeti 'nde yapılandırılan grubun ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="d49c8-145">The details of the Group configured in API Management service.</span></span>

### <span data-ttu-id="d49c8-146">IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup></span><span class="sxs-lookup"><span data-stu-id="d49c8-146">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>
<span data-ttu-id="d49c8-147">API Yönetim hizmetinde yapılandırılmış grupların listesi.</span><span class="sxs-lookup"><span data-stu-id="d49c8-147">The list of Groups configured in API Management service.</span></span>

## <span data-ttu-id="d49c8-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d49c8-148">NOTES</span></span>

## <span data-ttu-id="d49c8-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d49c8-149">RELATED LINKS</span></span>

[<span data-ttu-id="d49c8-150">Yeni-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="d49c8-150">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d49c8-151">Remove-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="d49c8-151">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="d49c8-152">Set-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="d49c8-152">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


