---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c8f05c7ca9ddeb5868d62633600d63f5d7f01be0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587325"
---
# <span data-ttu-id="a3e48-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="a3e48-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="a3e48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3e48-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e48-103">Kiracı erişimini etkinleştirilir veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a3e48-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3e48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3e48-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3e48-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3e48-105">DESCRIPTION</span></span>
<span data-ttu-id="a3e48-106">**Set-AzureRmApiManagementTenantAccess** cmdlet 'i kiracı erişimini devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a3e48-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="a3e48-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3e48-107">EXAMPLES</span></span>

### <span data-ttu-id="a3e48-108">Örnek 1: kiracı erişimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a3e48-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="a3e48-109">Bu komut, belirtilen bağlamda kiracı erişimini etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="a3e48-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="a3e48-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3e48-110">PARAMETERS</span></span>

### <span data-ttu-id="a3e48-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a3e48-111">-Context</span></span>
<span data-ttu-id="a3e48-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3e48-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a3e48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e48-113">-DefaultProfile</span></span>
<span data-ttu-id="a3e48-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3e48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3e48-115">Özellikli</span><span class="sxs-lookup"><span data-stu-id="a3e48-115">-Enabled</span></span>
<span data-ttu-id="a3e48-116">Bu cmdlet 'in kiracı erişimini etkinleştirip etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3e48-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="a3e48-117">Etkinleştirmek $False veya devre dışı bırakmak için $True değeri belirtin.</span><span class="sxs-lookup"><span data-stu-id="a3e48-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e48-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a3e48-118">-PassThru</span></span>
<span data-ttu-id="a3e48-119">Bu cmdlet 'in değiştirdiği **Psapsananagementaccessınformation** olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3e48-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a3e48-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e48-120">CommonParameters</span></span>
<span data-ttu-id="a3e48-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3e48-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e48-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3e48-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e48-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3e48-123">INPUTS</span></span>

### <span data-ttu-id="a3e48-124">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="a3e48-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a3e48-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a3e48-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a3e48-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3e48-126">OUTPUTS</span></span>

### <span data-ttu-id="a3e48-127">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="a3e48-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="a3e48-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3e48-128">NOTES</span></span>

## <span data-ttu-id="a3e48-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3e48-129">RELATED LINKS</span></span>

[<span data-ttu-id="a3e48-130">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="a3e48-130">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


