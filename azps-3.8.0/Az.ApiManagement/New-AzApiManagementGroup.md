---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 8f7d221ca4f90f67bce038015b4c654881dfa598
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097717"
---
# <span data-ttu-id="aa03c-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="aa03c-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="aa03c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa03c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa03c-103">Bir API yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aa03c-103">Creates an API management group.</span></span>

## <span data-ttu-id="aa03c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa03c-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa03c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa03c-105">DESCRIPTION</span></span>
<span data-ttu-id="aa03c-106">**Yeni-Azapsananagementgroup** cmdlet 'ı bir API yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aa03c-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="aa03c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa03c-107">EXAMPLES</span></span>

### <span data-ttu-id="aa03c-108">Örnek 1: yönetim grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="aa03c-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="aa03c-109">Bu komut bir yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aa03c-109">This command creates a management group.</span></span>

## <span data-ttu-id="aa03c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa03c-110">PARAMETERS</span></span>

### <span data-ttu-id="aa03c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="aa03c-111">-Context</span></span>
<span data-ttu-id="aa03c-112">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa03c-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="aa03c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa03c-113">-DefaultProfile</span></span>
<span data-ttu-id="aa03c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa03c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa03c-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="aa03c-115">-Description</span></span>
<span data-ttu-id="aa03c-116">Yönetim grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa03c-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="aa03c-117">-ExternalID</span><span class="sxs-lookup"><span data-stu-id="aa03c-117">-ExternalId</span></span>
<span data-ttu-id="aa03c-118">Dış gruplar için bu özellik, dış kimlik sağlayıcısından grubun kimliğini içerir; örneğin, Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; Aksi takdirde değer null olur.</span><span class="sxs-lookup"><span data-stu-id="aa03c-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="aa03c-119">-GroupID</span><span class="sxs-lookup"><span data-stu-id="aa03c-119">-GroupId</span></span>
<span data-ttu-id="aa03c-120">Yeni yönetim grubunun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa03c-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="aa03c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="aa03c-121">-Name</span></span>
<span data-ttu-id="aa03c-122">Yönetim grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa03c-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="aa03c-123">-Tür</span><span class="sxs-lookup"><span data-stu-id="aa03c-123">-Type</span></span>
<span data-ttu-id="aa03c-124">Grup türü.</span><span class="sxs-lookup"><span data-stu-id="aa03c-124">Group Type.</span></span> <span data-ttu-id="aa03c-125">Özel grup Kullanıcı tanımlı gruptur.</span><span class="sxs-lookup"><span data-stu-id="aa03c-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="aa03c-126">Sistem grubu yöneticiyi, geliştiricileri ve konukları içerir.</span><span class="sxs-lookup"><span data-stu-id="aa03c-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="aa03c-127">Sistem grubu oluşturamaz veya güncelleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa03c-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="aa03c-128">Dış Grup, Azure Active Directory gibi dış kimlik sağlayıcısından gelen gruplarıdır.</span><span class="sxs-lookup"><span data-stu-id="aa03c-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="aa03c-129">Bu parametre isteğe bağlıdır ve varsayılan olarak özel grup olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="aa03c-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

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

### <span data-ttu-id="aa03c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa03c-130">CommonParameters</span></span>
<span data-ttu-id="aa03c-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa03c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa03c-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aa03c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa03c-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa03c-133">INPUTS</span></span>

### <span data-ttu-id="aa03c-134">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="aa03c-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa03c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="aa03c-135">System.String</span></span>

### <span data-ttu-id="aa03c-136">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananayöneti. ServiceManagement. modeller. Psapsananagementgrouptype, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="aa03c-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="aa03c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa03c-137">OUTPUTS</span></span>

### <span data-ttu-id="aa03c-138">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="aa03c-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="aa03c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa03c-139">NOTES</span></span>

## <span data-ttu-id="aa03c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa03c-140">RELATED LINKS</span></span>

[<span data-ttu-id="aa03c-141">Get-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="aa03c-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="aa03c-142">Remove-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="aa03c-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="aa03c-143">Set-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="aa03c-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


