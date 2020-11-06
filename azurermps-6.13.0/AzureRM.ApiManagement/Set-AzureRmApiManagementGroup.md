---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 058a82398be387913a0dd3eaf58c80ac12b692dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587343"
---
# <span data-ttu-id="3f541-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3f541-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="3f541-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f541-102">SYNOPSIS</span></span>
<span data-ttu-id="3f541-103">Bir API yönetim grubu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="3f541-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f541-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f541-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f541-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f541-105">DESCRIPTION</span></span>
<span data-ttu-id="3f541-106">**Set-Azurermapımanagementgroup** cmdlet 'ı bir API yönetim grubu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="3f541-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="3f541-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f541-107">EXAMPLES</span></span>

### <span data-ttu-id="3f541-108">Örnek 1: yönetim grubu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3f541-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="3f541-109">Bu komut, Group0001 adlı bir yönetim grubunu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="3f541-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="3f541-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f541-110">PARAMETERS</span></span>

### <span data-ttu-id="3f541-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3f541-111">-Context</span></span>
<span data-ttu-id="3f541-112">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f541-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3f541-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f541-113">-DefaultProfile</span></span>
<span data-ttu-id="3f541-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3f541-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f541-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="3f541-115">-Description</span></span>
<span data-ttu-id="3f541-116">Yönetim grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f541-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="3f541-117">-GroupID</span><span class="sxs-lookup"><span data-stu-id="3f541-117">-GroupId</span></span>
<span data-ttu-id="3f541-118">Yönetim grubunun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f541-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="3f541-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3f541-119">-Name</span></span>
<span data-ttu-id="3f541-120">Yönetim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f541-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="3f541-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3f541-121">-PassThru</span></span>
<span data-ttu-id="3f541-122">geçiş</span><span class="sxs-lookup"><span data-stu-id="3f541-122">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f541-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f541-123">CommonParameters</span></span>
<span data-ttu-id="3f541-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f541-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f541-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f541-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f541-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f541-126">INPUTS</span></span>

### <span data-ttu-id="3f541-127">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="3f541-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3f541-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3f541-128">System.String</span></span>

### <span data-ttu-id="3f541-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3f541-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3f541-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f541-130">OUTPUTS</span></span>

### <span data-ttu-id="3f541-131">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="3f541-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="3f541-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f541-132">NOTES</span></span>

## <span data-ttu-id="3f541-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f541-133">RELATED LINKS</span></span>

[<span data-ttu-id="3f541-134">Get-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="3f541-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="3f541-135">Yeni-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="3f541-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="3f541-136">Remove-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="3f541-136">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


