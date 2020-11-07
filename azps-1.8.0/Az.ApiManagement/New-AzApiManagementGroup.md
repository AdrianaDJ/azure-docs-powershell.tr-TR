---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 22feec8308b682aa2290de6bd8b7361bb07cd560
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761672"
---
# <span data-ttu-id="e0751-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e0751-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="e0751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0751-102">SYNOPSIS</span></span>
<span data-ttu-id="e0751-103">Bir API yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0751-103">Creates an API management group.</span></span>

## <span data-ttu-id="e0751-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0751-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0751-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0751-105">DESCRIPTION</span></span>
<span data-ttu-id="e0751-106">**Yeni-Azapsananagementgroup** cmdlet 'ı bir API yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0751-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="e0751-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0751-107">EXAMPLES</span></span>

### <span data-ttu-id="e0751-108">Örnek 1: yönetim grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="e0751-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="e0751-109">Bu komut bir yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0751-109">This command creates a management group.</span></span>

## <span data-ttu-id="e0751-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0751-110">PARAMETERS</span></span>

### <span data-ttu-id="e0751-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e0751-111">-Context</span></span>
<span data-ttu-id="e0751-112">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0751-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e0751-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0751-113">-DefaultProfile</span></span>
<span data-ttu-id="e0751-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0751-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0751-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e0751-115">-Description</span></span>
<span data-ttu-id="e0751-116">Yönetim grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0751-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="e0751-117">-ExternalID</span><span class="sxs-lookup"><span data-stu-id="e0751-117">-ExternalId</span></span>
<span data-ttu-id="e0751-118">Dış gruplar için bu özellik, dış kimlik sağlayıcısından grubun kimliğini içerir; örneğin, Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; Aksi takdirde değer null olur.</span><span class="sxs-lookup"><span data-stu-id="e0751-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="e0751-119">-GroupID</span><span class="sxs-lookup"><span data-stu-id="e0751-119">-GroupId</span></span>
<span data-ttu-id="e0751-120">Yeni yönetim grubunun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0751-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="e0751-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0751-121">-Name</span></span>
<span data-ttu-id="e0751-122">Yönetim grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0751-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="e0751-123">-Tür</span><span class="sxs-lookup"><span data-stu-id="e0751-123">-Type</span></span>
<span data-ttu-id="e0751-124">Grup türü.</span><span class="sxs-lookup"><span data-stu-id="e0751-124">Group Type.</span></span> <span data-ttu-id="e0751-125">Özel grup Kullanıcı tanımlı gruptur.</span><span class="sxs-lookup"><span data-stu-id="e0751-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="e0751-126">Sistem grubu yöneticiyi, geliştiricileri ve konukları içerir.</span><span class="sxs-lookup"><span data-stu-id="e0751-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="e0751-127">Sistem grubu oluşturamaz veya güncelleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="e0751-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="e0751-128">Dış Grup, Azure Active Directory gibi dış kimlik sağlayıcısından gelen gruplarıdır.</span><span class="sxs-lookup"><span data-stu-id="e0751-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="e0751-129">Bu parametre isteğe bağlıdır ve varsayılan olarak özel grup olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="e0751-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System, External

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0751-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0751-130">CommonParameters</span></span>
<span data-ttu-id="e0751-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0751-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0751-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0751-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0751-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0751-133">INPUTS</span></span>

### <span data-ttu-id="e0751-134">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e0751-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e0751-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e0751-135">System.String</span></span>

### <span data-ttu-id="e0751-136">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananayöneti. ServiceManagement. modeller. Psapsananagementgrouptype, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="e0751-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e0751-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0751-137">OUTPUTS</span></span>

### <span data-ttu-id="e0751-138">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="e0751-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="e0751-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0751-139">NOTES</span></span>

## <span data-ttu-id="e0751-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0751-140">RELATED LINKS</span></span>

[<span data-ttu-id="e0751-141">Get-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="e0751-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="e0751-142">Remove-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="e0751-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="e0751-143">Set-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="e0751-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


