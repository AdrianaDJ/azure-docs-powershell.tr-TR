---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0c28742eb3c774adb8c7b6a8d920e91377bea35f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591840"
---
# <span data-ttu-id="678a9-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="678a9-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="678a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="678a9-102">SYNOPSIS</span></span>
<span data-ttu-id="678a9-103">Tüm veya belirli API Yönetim gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="678a9-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="678a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="678a9-104">SYNTAX</span></span>

### <span data-ttu-id="678a9-105">Tüm grupları Al (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="678a9-105">Get all groups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678a9-106">Grup KIMLIĞINE göre al</span><span class="sxs-lookup"><span data-stu-id="678a9-106">Get by group ID</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678a9-107">Kullanıcıları kullanıcıya göre bulma</span><span class="sxs-lookup"><span data-stu-id="678a9-107">Find groups by user</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678a9-108">Ürünlere göre grupları bulma</span><span class="sxs-lookup"><span data-stu-id="678a9-108">Find groups by product</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="678a9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="678a9-109">DESCRIPTION</span></span>
<span data-ttu-id="678a9-110">**Get-Azurermapımanagementgroup** cmdlet 'i veya belirli API Yönetim gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="678a9-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="678a9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="678a9-111">EXAMPLES</span></span>

### <span data-ttu-id="678a9-112">Örnek 1: tüm grupları Al</span><span class="sxs-lookup"><span data-stu-id="678a9-112">Example 1: Get all groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext
```

<span data-ttu-id="678a9-113">Bu komut tüm grupları alır.</span><span class="sxs-lookup"><span data-stu-id="678a9-113">This command gets all groups.</span></span>

### <span data-ttu-id="678a9-114">Örnek 2: bir grup KIMLIĞI alma</span><span class="sxs-lookup"><span data-stu-id="678a9-114">Example 2: Get a group by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -GroupId "0123456789"
```

<span data-ttu-id="678a9-115">Bu komut, 0123456789 adlı grup KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="678a9-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="678a9-116">Örnek 3: ada göre grupla</span><span class="sxs-lookup"><span data-stu-id="678a9-116">Example 3: Get a group by name</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -Name "Group0002"
```

<span data-ttu-id="678a9-117">Bu komut, Group0002 adlı grubu alır.</span><span class="sxs-lookup"><span data-stu-id="678a9-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="678a9-118">Örnek 4: tüm Kullanıcı gruplarını alma</span><span class="sxs-lookup"><span data-stu-id="678a9-118">Example 4: Get all user groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -UserId "0123456789"
```

<span data-ttu-id="678a9-119">Bu komut, 0123456789 adlı Kullanıcı KIMLIĞINE sahip tüm Kullanıcı gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="678a9-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="678a9-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="678a9-120">PARAMETERS</span></span>

### <span data-ttu-id="678a9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="678a9-121">-Context</span></span>
<span data-ttu-id="678a9-122">Psapsananagementcontext örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="678a9-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="678a9-123">-GroupID</span><span class="sxs-lookup"><span data-stu-id="678a9-123">-GroupId</span></span>
<span data-ttu-id="678a9-124">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="678a9-124">Specifies the group ID.</span></span>
<span data-ttu-id="678a9-125">Belirtilmişse, cmdlet tanıtıcıyı tanımlayıcı tarafından bulmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="678a9-125">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by group ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678a9-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="678a9-126">-Name</span></span>
<span data-ttu-id="678a9-127">Yönetim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="678a9-127">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="678a9-128">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="678a9-128">-ProductId</span></span>
<span data-ttu-id="678a9-129">Var olan ürünün tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="678a9-129">Identifier of existing product.</span></span>
<span data-ttu-id="678a9-130">Belirtilirse, ürünün atandığı tüm grupları döndürür.</span><span class="sxs-lookup"><span data-stu-id="678a9-130">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="678a9-131">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="678a9-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by product
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678a9-132">-UserID</span><span class="sxs-lookup"><span data-stu-id="678a9-132">-UserId</span></span>
<span data-ttu-id="678a9-133">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="678a9-133">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="678a9-134">Belirtilmişse cmdlet, ürünün atandığı tüm grupları döndürür.</span><span class="sxs-lookup"><span data-stu-id="678a9-134">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by user
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678a9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678a9-135">-DefaultProfile</span></span>
<span data-ttu-id="678a9-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="678a9-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="678a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678a9-137">CommonParameters</span></span>
<span data-ttu-id="678a9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="678a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678a9-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678a9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678a9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="678a9-140">INPUTS</span></span>

## <span data-ttu-id="678a9-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="678a9-141">OUTPUTS</span></span>

### <span data-ttu-id="678a9-142">IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup></span><span class="sxs-lookup"><span data-stu-id="678a9-142">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>

## <span data-ttu-id="678a9-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="678a9-143">NOTES</span></span>

## <span data-ttu-id="678a9-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="678a9-144">RELATED LINKS</span></span>

[<span data-ttu-id="678a9-145">Yeni-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="678a9-145">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="678a9-146">Remove-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="678a9-146">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="678a9-147">Set-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="678a9-147">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


