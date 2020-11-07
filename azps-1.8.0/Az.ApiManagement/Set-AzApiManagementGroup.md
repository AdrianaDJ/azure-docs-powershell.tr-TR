---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: 027e07ed495cb5b80fbd05852b640526c87bf16e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917692"
---
# <span data-ttu-id="20eec-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="20eec-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="20eec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20eec-102">SYNOPSIS</span></span>
<span data-ttu-id="20eec-103">Bir API yönetim grubu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="20eec-103">Configures an API management group.</span></span>

## <span data-ttu-id="20eec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20eec-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20eec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="20eec-105">DESCRIPTION</span></span>
<span data-ttu-id="20eec-106">**Set-Azapsananagementgroup** cmdlet 'ı bir API yönetim grubu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="20eec-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="20eec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20eec-107">EXAMPLES</span></span>

### <span data-ttu-id="20eec-108">Örnek 1: yönetim grubu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="20eec-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="20eec-109">Bu komut, Group0001 adlı bir yönetim grubunu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="20eec-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="20eec-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20eec-110">PARAMETERS</span></span>

### <span data-ttu-id="20eec-111">-Context</span><span class="sxs-lookup"><span data-stu-id="20eec-111">-Context</span></span>
<span data-ttu-id="20eec-112">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="20eec-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="20eec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20eec-113">-DefaultProfile</span></span>
<span data-ttu-id="20eec-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20eec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20eec-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="20eec-115">-Description</span></span>
<span data-ttu-id="20eec-116">Yönetim grubunun açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20eec-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="20eec-117">-GroupID</span><span class="sxs-lookup"><span data-stu-id="20eec-117">-GroupId</span></span>
<span data-ttu-id="20eec-118">Yönetim grubunun tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20eec-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="20eec-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="20eec-119">-Name</span></span>
<span data-ttu-id="20eec-120">Yönetim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20eec-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="20eec-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="20eec-121">-PassThru</span></span>
<span data-ttu-id="20eec-122">geçiş</span><span class="sxs-lookup"><span data-stu-id="20eec-122">passthru</span></span>

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

### <span data-ttu-id="20eec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20eec-123">CommonParameters</span></span>
<span data-ttu-id="20eec-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20eec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20eec-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20eec-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20eec-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20eec-126">INPUTS</span></span>

### <span data-ttu-id="20eec-127">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="20eec-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="20eec-128">System. String</span><span class="sxs-lookup"><span data-stu-id="20eec-128">System.String</span></span>

### <span data-ttu-id="20eec-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="20eec-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="20eec-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20eec-130">OUTPUTS</span></span>

### <span data-ttu-id="20eec-131">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="20eec-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="20eec-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20eec-132">NOTES</span></span>

## <span data-ttu-id="20eec-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20eec-133">RELATED LINKS</span></span>

[<span data-ttu-id="20eec-134">Get-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="20eec-134">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="20eec-135">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="20eec-135">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="20eec-136">Remove-Azapsananagementgroup</span><span class="sxs-lookup"><span data-stu-id="20eec-136">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


