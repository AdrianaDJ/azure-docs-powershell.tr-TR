---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 08bbb81998107a11a5996cb75a6fba8b760802db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104167"
---
# <span data-ttu-id="64d71-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="64d71-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="64d71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64d71-102">SYNOPSIS</span></span>
<span data-ttu-id="64d71-103">Kiracı erişimini etkinleştirilir veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="64d71-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="64d71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64d71-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64d71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64d71-105">DESCRIPTION</span></span>
<span data-ttu-id="64d71-106">**Set-AzApiManagementTenantAccess** cmdlet 'i kiracı erişimini devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="64d71-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="64d71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64d71-107">EXAMPLES</span></span>

### <span data-ttu-id="64d71-108">Örnek 1: kiracı erişimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="64d71-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="64d71-109">Bu komut, belirtilen bağlamda kiracı erişimini etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="64d71-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="64d71-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64d71-110">PARAMETERS</span></span>

### <span data-ttu-id="64d71-111">-Context</span><span class="sxs-lookup"><span data-stu-id="64d71-111">-Context</span></span>
<span data-ttu-id="64d71-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="64d71-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="64d71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d71-113">-DefaultProfile</span></span>
<span data-ttu-id="64d71-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64d71-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64d71-115">Özellikli</span><span class="sxs-lookup"><span data-stu-id="64d71-115">-Enabled</span></span>
<span data-ttu-id="64d71-116">Bu cmdlet 'in kiracı erişimini etkinleştirip etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="64d71-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="64d71-117">Etkinleştirmek $False veya devre dışı bırakmak için $True değeri belirtin.</span><span class="sxs-lookup"><span data-stu-id="64d71-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="64d71-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="64d71-118">-PassThru</span></span>
<span data-ttu-id="64d71-119">Bu cmdlet 'in değiştirdiği **Psapsananagementaccessınformation** olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="64d71-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="64d71-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d71-120">CommonParameters</span></span>
<span data-ttu-id="64d71-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64d71-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d71-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="64d71-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d71-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64d71-123">INPUTS</span></span>

### <span data-ttu-id="64d71-124">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="64d71-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="64d71-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="64d71-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="64d71-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64d71-126">OUTPUTS</span></span>

### <span data-ttu-id="64d71-127">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="64d71-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="64d71-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64d71-128">NOTES</span></span>

## <span data-ttu-id="64d71-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64d71-129">RELATED LINKS</span></span>

[<span data-ttu-id="64d71-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="64d71-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


