---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0443b9bc3ed2666600f2d119eca5b7173b21e89d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764198"
---
# <span data-ttu-id="fb348-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fb348-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="fb348-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb348-102">SYNOPSIS</span></span>
<span data-ttu-id="fb348-103">Bir API yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb348-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb348-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb348-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb348-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb348-105">DESCRIPTION</span></span>
<span data-ttu-id="fb348-106">**Yeni-Azurermapımanagementgroup** cmdlet 'ı bir API yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb348-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="fb348-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb348-107">EXAMPLES</span></span>

### <span data-ttu-id="fb348-108">Örnek 1: yönetim grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="fb348-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="fb348-109">Bu komut bir yönetim grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fb348-109">This command creates a management group.</span></span>

## <span data-ttu-id="fb348-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb348-110">PARAMETERS</span></span>

### <span data-ttu-id="fb348-111">-Context</span><span class="sxs-lookup"><span data-stu-id="fb348-111">-Context</span></span>
<span data-ttu-id="fb348-112">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb348-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fb348-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb348-113">-DefaultProfile</span></span>
<span data-ttu-id="fb348-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb348-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="fb348-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="fb348-115">-Description</span></span>
<span data-ttu-id="fb348-116">Yönetim grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb348-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="fb348-117">-ExternalID</span><span class="sxs-lookup"><span data-stu-id="fb348-117">-ExternalId</span></span>
<span data-ttu-id="fb348-118">Dış gruplar için bu özellik, dış kimlik sağlayıcısından grubun kimliğini içerir; örneğin, Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; Aksi takdirde değer null olur.</span><span class="sxs-lookup"><span data-stu-id="fb348-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb348-119">-GroupID</span><span class="sxs-lookup"><span data-stu-id="fb348-119">-GroupId</span></span>
<span data-ttu-id="fb348-120">Yeni yönetim grubunun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb348-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="fb348-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb348-121">-Name</span></span>
<span data-ttu-id="fb348-122">Yönetim grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fb348-122">Specifies the management group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb348-123">-Tür</span><span class="sxs-lookup"><span data-stu-id="fb348-123">-Type</span></span>
<span data-ttu-id="fb348-124">Grup türü.</span><span class="sxs-lookup"><span data-stu-id="fb348-124">Group Type.</span></span> <span data-ttu-id="fb348-125">Özel grup Kullanıcı tanımlı gruptur.</span><span class="sxs-lookup"><span data-stu-id="fb348-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="fb348-126">Sistem grubu yöneticiyi, geliştiricileri ve konukları içerir.</span><span class="sxs-lookup"><span data-stu-id="fb348-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="fb348-127">Sistem grubu oluşturamaz veya güncelleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb348-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="fb348-128">Dış Grup, Azure Active Directory gibi dış kimlik sağlayıcısından gelen gruplarıdır.</span><span class="sxs-lookup"><span data-stu-id="fb348-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="fb348-129">Bu parametre isteğe bağlıdır ve varsayılan olarak özel grup olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="fb348-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: PsApiManagementGroupType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb348-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb348-130">CommonParameters</span></span>
<span data-ttu-id="fb348-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb348-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb348-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb348-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb348-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb348-133">INPUTS</span></span>

### <span data-ttu-id="fb348-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fb348-134">None</span></span>
<span data-ttu-id="fb348-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="fb348-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb348-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb348-136">OUTPUTS</span></span>

### <span data-ttu-id="fb348-137">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="fb348-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="fb348-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb348-138">NOTES</span></span>

## <span data-ttu-id="fb348-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb348-139">RELATED LINKS</span></span>

[<span data-ttu-id="fb348-140">Get-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="fb348-140">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="fb348-141">Remove-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="fb348-141">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="fb348-142">Set-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="fb348-142">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


