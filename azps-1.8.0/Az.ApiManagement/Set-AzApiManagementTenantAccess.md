---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 5f14a0698c0b1ea950a28236a8a523734b2ddf5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917672"
---
# <span data-ttu-id="8a40c-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="8a40c-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="8a40c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a40c-102">SYNOPSIS</span></span>
<span data-ttu-id="8a40c-103">Kiracı erişimini etkinleştirilir veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8a40c-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="8a40c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a40c-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a40c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a40c-105">DESCRIPTION</span></span>
<span data-ttu-id="8a40c-106">**Set-AzApiManagementTenantAccess** cmdlet 'i kiracı erişimini devre dışı bırakır veya devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8a40c-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="8a40c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a40c-107">EXAMPLES</span></span>

### <span data-ttu-id="8a40c-108">Örnek 1: kiracı erişimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="8a40c-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="8a40c-109">Bu komut, belirtilen bağlamda kiracı erişimini etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="8a40c-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="8a40c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a40c-110">PARAMETERS</span></span>

### <span data-ttu-id="8a40c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8a40c-111">-Context</span></span>
<span data-ttu-id="8a40c-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a40c-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8a40c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a40c-113">-DefaultProfile</span></span>
<span data-ttu-id="8a40c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a40c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a40c-115">Özellikli</span><span class="sxs-lookup"><span data-stu-id="8a40c-115">-Enabled</span></span>
<span data-ttu-id="8a40c-116">Bu cmdlet 'in kiracı erişimini etkinleştirip etkinleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a40c-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="8a40c-117">Etkinleştirmek $False veya devre dışı bırakmak için $True değeri belirtin.</span><span class="sxs-lookup"><span data-stu-id="8a40c-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="8a40c-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8a40c-118">-PassThru</span></span>
<span data-ttu-id="8a40c-119">Bu cmdlet 'in değiştirdiği **Psapsananagementaccessınformation** olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a40c-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8a40c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a40c-120">CommonParameters</span></span>
<span data-ttu-id="8a40c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a40c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a40c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a40c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a40c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a40c-123">INPUTS</span></span>

### <span data-ttu-id="8a40c-124">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="8a40c-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8a40c-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8a40c-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8a40c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a40c-126">OUTPUTS</span></span>

### <span data-ttu-id="8a40c-127">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccessınformation</span><span class="sxs-lookup"><span data-stu-id="8a40c-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="8a40c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a40c-128">NOTES</span></span>

## <span data-ttu-id="8a40c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a40c-129">RELATED LINKS</span></span>

[<span data-ttu-id="8a40c-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="8a40c-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


