---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 99c5cef4a15619da455b3e7ba1c7891652b991f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593845"
---
# <span data-ttu-id="36f9e-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="36f9e-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="36f9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="36f9e-103">Bir API yönetim grubu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="36f9e-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36f9e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36f9e-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36f9e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="36f9e-105">DESCRIPTION</span></span>
<span data-ttu-id="36f9e-106">**Set-Azurermapımanagementgroup** cmdlet 'ı bir API yönetim grubu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="36f9e-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="36f9e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36f9e-107">EXAMPLES</span></span>

### <span data-ttu-id="36f9e-108">Örnek 1: yönetim grubu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="36f9e-108">Example 1: Configure a management group</span></span>
```
PS C:\>Set-AzureRmApiManagementGroup -Context $APImContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="36f9e-109">Bu komut, Group0001 adlı bir yönetim grubunu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="36f9e-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="36f9e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36f9e-110">PARAMETERS</span></span>

### <span data-ttu-id="36f9e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="36f9e-111">-Context</span></span>
<span data-ttu-id="36f9e-112">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f9e-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="36f9e-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="36f9e-113">-Description</span></span>
<span data-ttu-id="36f9e-114">Yönetim grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f9e-114">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="36f9e-115">-GroupID</span><span class="sxs-lookup"><span data-stu-id="36f9e-115">-GroupId</span></span>
<span data-ttu-id="36f9e-116">Yönetim grubunun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f9e-116">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="36f9e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="36f9e-117">-Name</span></span>
<span data-ttu-id="36f9e-118">Yönetim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f9e-118">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="36f9e-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="36f9e-119">-PassThru</span></span>
<span data-ttu-id="36f9e-120">geçiş</span><span class="sxs-lookup"><span data-stu-id="36f9e-120">passthru</span></span>

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

### <span data-ttu-id="36f9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f9e-121">-DefaultProfile</span></span>
<span data-ttu-id="36f9e-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36f9e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36f9e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f9e-123">CommonParameters</span></span>
<span data-ttu-id="36f9e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36f9e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f9e-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36f9e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f9e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36f9e-126">INPUTS</span></span>

## <span data-ttu-id="36f9e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36f9e-127">OUTPUTS</span></span>

### <span data-ttu-id="36f9e-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="36f9e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="36f9e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36f9e-129">NOTES</span></span>

## <span data-ttu-id="36f9e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36f9e-130">RELATED LINKS</span></span>

[<span data-ttu-id="36f9e-131">Get-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="36f9e-131">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="36f9e-132">Yeni-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="36f9e-132">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="36f9e-133">Remove-Azurermapımanagementgroup</span><span class="sxs-lookup"><span data-stu-id="36f9e-133">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


