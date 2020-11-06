---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: abb86f40c9ac4a2ca04e0f14500df6c39e550dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592831"
---
# <span data-ttu-id="10693-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="10693-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="10693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10693-102">SYNOPSIS</span></span>
<span data-ttu-id="10693-103">Gruba bir kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="10693-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10693-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10693-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10693-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10693-105">DESCRIPTION</span></span>
<span data-ttu-id="10693-106">**Add-Azurermapımanagementusertogroup** cmdlet 'i bir gruba kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="10693-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="10693-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10693-107">EXAMPLES</span></span>

### <span data-ttu-id="10693-108">Örnek 1: gruba kullanıcı ekleme</span><span class="sxs-lookup"><span data-stu-id="10693-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="10693-109">Bu komut mevcut bir gruba varolan bir kullanıcıyı ekler.</span><span class="sxs-lookup"><span data-stu-id="10693-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="10693-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10693-110">PARAMETERS</span></span>

### <span data-ttu-id="10693-111">-Context</span><span class="sxs-lookup"><span data-stu-id="10693-111">-Context</span></span>
<span data-ttu-id="10693-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10693-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="10693-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="10693-113">This parameter is required.</span></span>

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

### <span data-ttu-id="10693-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10693-114">-DefaultProfile</span></span>
<span data-ttu-id="10693-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10693-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10693-116">-GroupID</span><span class="sxs-lookup"><span data-stu-id="10693-116">-GroupId</span></span>
<span data-ttu-id="10693-117">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="10693-117">Specifies the group ID.</span></span>
<span data-ttu-id="10693-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="10693-118">This parameter is required.</span></span>

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

### <span data-ttu-id="10693-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="10693-119">-PassThru</span></span>
<span data-ttu-id="10693-120">geçiş</span><span class="sxs-lookup"><span data-stu-id="10693-120">passthru</span></span>

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

### <span data-ttu-id="10693-121">-UserID</span><span class="sxs-lookup"><span data-stu-id="10693-121">-UserId</span></span>
<span data-ttu-id="10693-122">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="10693-122">Specifies the user ID.</span></span>
<span data-ttu-id="10693-123">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="10693-123">This parameter is required.</span></span>

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

### <span data-ttu-id="10693-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10693-124">CommonParameters</span></span>
<span data-ttu-id="10693-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10693-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10693-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10693-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10693-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10693-127">INPUTS</span></span>

### <span data-ttu-id="10693-128">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="10693-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="10693-129">System. String</span><span class="sxs-lookup"><span data-stu-id="10693-129">System.String</span></span>

### <span data-ttu-id="10693-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="10693-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="10693-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10693-131">OUTPUTS</span></span>

### <span data-ttu-id="10693-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10693-132">System.Boolean</span></span>

## <span data-ttu-id="10693-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10693-133">NOTES</span></span>

## <span data-ttu-id="10693-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10693-134">RELATED LINKS</span></span>

[<span data-ttu-id="10693-135">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="10693-135">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="10693-136">Remove-Azurermapımanagementuserfromgroup</span><span class="sxs-lookup"><span data-stu-id="10693-136">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


