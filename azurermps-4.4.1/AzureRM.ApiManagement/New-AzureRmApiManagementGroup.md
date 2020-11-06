---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 8fc237b130e5044e52f47d306d04c42d12fbad81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591226"
---
# <span data-ttu-id="23047-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="23047-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="23047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23047-102">SYNOPSIS</span></span>
<span data-ttu-id="23047-103">Bir API yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23047-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23047-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23047-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23047-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23047-105">DESCRIPTION</span></span>
<span data-ttu-id="23047-106">**Yeni-Azurermapımanagementgroup** cmdlet 'ı bir API yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23047-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="23047-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23047-107">EXAMPLES</span></span>

### <span data-ttu-id="23047-108">Örnek 1: yönetim grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="23047-108">Example 1: Create a management group</span></span>
```
PS C:\>New-AzureRmApiManagementGroup -Context $APImContext -Name "Group0001"
```

<span data-ttu-id="23047-109">Bu komut bir yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23047-109">This command creates a management group.</span></span>

## <span data-ttu-id="23047-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23047-110">PARAMETERS</span></span>

### <span data-ttu-id="23047-111">-Context</span><span class="sxs-lookup"><span data-stu-id="23047-111">-Context</span></span>
<span data-ttu-id="23047-112">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23047-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="23047-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="23047-113">-Description</span></span>
<span data-ttu-id="23047-114">Yönetim grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23047-114">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="23047-115">-ExternalID</span><span class="sxs-lookup"><span data-stu-id="23047-115">-ExternalId</span></span>
<span data-ttu-id="23047-116">Dış gruplar için bu özellik, dış kimlik sağlayıcısından grubun kimliğini içerir; örneğin, Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; Aksi takdirde değer null olur.</span><span class="sxs-lookup"><span data-stu-id="23047-116">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="23047-117">-GroupID</span><span class="sxs-lookup"><span data-stu-id="23047-117">-GroupId</span></span>
<span data-ttu-id="23047-118">Yeni yönetim grubunun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23047-118">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="23047-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="23047-119">-Name</span></span>
<span data-ttu-id="23047-120">Yönetim grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23047-120">Specifies the management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23047-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="23047-121">-Type</span></span>
<span data-ttu-id="23047-122">Grup türü.</span><span class="sxs-lookup"><span data-stu-id="23047-122">Group Type.</span></span> <span data-ttu-id="23047-123">Özel grup Kullanıcı tanımlı gruptur.</span><span class="sxs-lookup"><span data-stu-id="23047-123">Custom Group is User defined Group.</span></span> <span data-ttu-id="23047-124">Sistem grubu yöneticiyi, geliştiricileri ve konukları içerir.</span><span class="sxs-lookup"><span data-stu-id="23047-124">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="23047-125">Sistem grubu oluşturamaz veya güncelleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="23047-125">You cannot create or update a System Group.</span></span>  <span data-ttu-id="23047-126">Dış Grup, Azure Active Directory gibi dış kimlik sağlayıcısından gelen gruplarıdır.</span><span class="sxs-lookup"><span data-stu-id="23047-126">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="23047-127">Bu parametre isteğe bağlıdır ve varsayılan olarak özel grup olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="23047-127">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23047-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23047-128">-DefaultProfile</span></span>
<span data-ttu-id="23047-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23047-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23047-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23047-130">CommonParameters</span></span>
<span data-ttu-id="23047-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23047-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23047-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23047-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23047-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23047-133">INPUTS</span></span>

## <span data-ttu-id="23047-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23047-134">OUTPUTS</span></span>

### <span data-ttu-id="23047-135">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="23047-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="23047-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23047-136">NOTES</span></span>

## <span data-ttu-id="23047-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23047-137">RELATED LINKS</span></span>

[<span data-ttu-id="23047-138">Get-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="23047-138">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="23047-139">Remove-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="23047-139">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="23047-140">Set-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="23047-140">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


