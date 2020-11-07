---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 2d33ece97d2a0ef007b5970afef499fbb6f2117e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751187"
---
# <span data-ttu-id="5fd7b-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="5fd7b-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="5fd7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fd7b-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd7b-103">Gruba bir kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="5fd7b-103">Adds a user to a group.</span></span>

## <span data-ttu-id="5fd7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5fd7b-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fd7b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5fd7b-105">DESCRIPTION</span></span>
<span data-ttu-id="5fd7b-106">**Add-Azapsananagementusertogroup** cmdlet 'i bir gruba kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="5fd7b-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="5fd7b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5fd7b-107">EXAMPLES</span></span>

### <span data-ttu-id="5fd7b-108">Örnek 1: gruba kullanıcı ekleme</span><span class="sxs-lookup"><span data-stu-id="5fd7b-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="5fd7b-109">Bu komut mevcut bir gruba varolan bir kullanıcıyı ekler.</span><span class="sxs-lookup"><span data-stu-id="5fd7b-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="5fd7b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5fd7b-110">PARAMETERS</span></span>

### <span data-ttu-id="5fd7b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5fd7b-111">-Context</span></span>
<span data-ttu-id="5fd7b-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fd7b-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="5fd7b-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5fd7b-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5fd7b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd7b-114">-DefaultProfile</span></span>
<span data-ttu-id="5fd7b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5fd7b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fd7b-116">-GroupID</span><span class="sxs-lookup"><span data-stu-id="5fd7b-116">-GroupId</span></span>
<span data-ttu-id="5fd7b-117">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fd7b-117">Specifies the group ID.</span></span>
<span data-ttu-id="5fd7b-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5fd7b-118">This parameter is required.</span></span>

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

### <span data-ttu-id="5fd7b-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5fd7b-119">-PassThru</span></span>
<span data-ttu-id="5fd7b-120">geçiş</span><span class="sxs-lookup"><span data-stu-id="5fd7b-120">passthru</span></span>

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

### <span data-ttu-id="5fd7b-121">-UserID</span><span class="sxs-lookup"><span data-stu-id="5fd7b-121">-UserId</span></span>
<span data-ttu-id="5fd7b-122">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5fd7b-122">Specifies the user ID.</span></span>
<span data-ttu-id="5fd7b-123">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5fd7b-123">This parameter is required.</span></span>

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

### <span data-ttu-id="5fd7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd7b-124">CommonParameters</span></span>
<span data-ttu-id="5fd7b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5fd7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd7b-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fd7b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd7b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5fd7b-127">INPUTS</span></span>

### <span data-ttu-id="5fd7b-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="5fd7b-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5fd7b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5fd7b-129">System.String</span></span>

### <span data-ttu-id="5fd7b-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5fd7b-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5fd7b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5fd7b-131">OUTPUTS</span></span>

### <span data-ttu-id="5fd7b-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5fd7b-132">System.Boolean</span></span>

## <span data-ttu-id="5fd7b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5fd7b-133">NOTES</span></span>

## <span data-ttu-id="5fd7b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5fd7b-134">RELATED LINKS</span></span>

[<span data-ttu-id="5fd7b-135">Get-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="5fd7b-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="5fd7b-136">Remove-Azapsananagementuserfromgroup</span><span class="sxs-lookup"><span data-stu-id="5fd7b-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


