---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: d405dc21719abc1aec5767f4d1b89a938b79eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588323"
---
# <span data-ttu-id="69f1d-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="69f1d-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="69f1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="69f1d-103">Gruba bir kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="69f1d-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69f1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69f1d-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69f1d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69f1d-105">DESCRIPTION</span></span>
<span data-ttu-id="69f1d-106">**Add-Azurermapımanagementusertogroup** cmdlet 'i bir gruba kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="69f1d-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="69f1d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69f1d-107">EXAMPLES</span></span>

### <span data-ttu-id="69f1d-108">Örnek 1: gruba kullanıcı ekleme</span><span class="sxs-lookup"><span data-stu-id="69f1d-108">Example 1: Add a user to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="69f1d-109">Bu komut mevcut bir gruba varolan bir kullanıcıyı ekler.</span><span class="sxs-lookup"><span data-stu-id="69f1d-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="69f1d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69f1d-110">PARAMETERS</span></span>

### <span data-ttu-id="69f1d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="69f1d-111">-Context</span></span>
<span data-ttu-id="69f1d-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="69f1d-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="69f1d-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="69f1d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="69f1d-114">-GroupID</span><span class="sxs-lookup"><span data-stu-id="69f1d-114">-GroupId</span></span>
<span data-ttu-id="69f1d-115">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="69f1d-115">Specifies the group ID.</span></span>
<span data-ttu-id="69f1d-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="69f1d-116">This parameter is required.</span></span>

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

### <span data-ttu-id="69f1d-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="69f1d-117">-PassThru</span></span>
<span data-ttu-id="69f1d-118">geçiş</span><span class="sxs-lookup"><span data-stu-id="69f1d-118">passthru</span></span>

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

### <span data-ttu-id="69f1d-119">-UserID</span><span class="sxs-lookup"><span data-stu-id="69f1d-119">-UserId</span></span>
<span data-ttu-id="69f1d-120">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="69f1d-120">Specifies the user ID.</span></span>
<span data-ttu-id="69f1d-121">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="69f1d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="69f1d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f1d-122">-DefaultProfile</span></span>
<span data-ttu-id="69f1d-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69f1d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69f1d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f1d-124">CommonParameters</span></span>
<span data-ttu-id="69f1d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69f1d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f1d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69f1d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f1d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69f1d-127">INPUTS</span></span>

## <span data-ttu-id="69f1d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69f1d-128">OUTPUTS</span></span>

### <span data-ttu-id="69f1d-129">Boole</span><span class="sxs-lookup"><span data-stu-id="69f1d-129">Boolean</span></span>

## <span data-ttu-id="69f1d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69f1d-130">NOTES</span></span>

## <span data-ttu-id="69f1d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69f1d-131">RELATED LINKS</span></span>

[<span data-ttu-id="69f1d-132">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="69f1d-132">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="69f1d-133">Remove-Azurermapımanagementuserfromgroup</span><span class="sxs-lookup"><span data-stu-id="69f1d-133">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


