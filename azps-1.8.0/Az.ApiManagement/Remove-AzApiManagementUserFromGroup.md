---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 20c6894f91e92c6f70f5f753d26fe4d76a391e70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917735"
---
# <span data-ttu-id="464c5-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="464c5-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="464c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="464c5-102">SYNOPSIS</span></span>
<span data-ttu-id="464c5-103">Kullanıcıyı gruptan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="464c5-103">Removes a user from a group.</span></span>

## <span data-ttu-id="464c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="464c5-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="464c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="464c5-105">DESCRIPTION</span></span>
<span data-ttu-id="464c5-106">**Remove-Azapsananagementuserfromgroup** cmdlet 'i, bir kullanıcıyı var olan bir gruptan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="464c5-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="464c5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="464c5-107">EXAMPLES</span></span>

### <span data-ttu-id="464c5-108">Örnek 1: gruptan kullanıcı kaldırma</span><span class="sxs-lookup"><span data-stu-id="464c5-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="464c5-109">Bu komut, bir kullanıcıyı gruptan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="464c5-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="464c5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="464c5-110">PARAMETERS</span></span>

### <span data-ttu-id="464c5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="464c5-111">-Context</span></span>
<span data-ttu-id="464c5-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="464c5-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="464c5-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="464c5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="464c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="464c5-114">-DefaultProfile</span></span>
<span data-ttu-id="464c5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="464c5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="464c5-116">-GroupID</span><span class="sxs-lookup"><span data-stu-id="464c5-116">-GroupId</span></span>
<span data-ttu-id="464c5-117">Kullanıcının kaldırılacağı grubun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="464c5-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="464c5-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="464c5-118">-PassThru</span></span>
<span data-ttu-id="464c5-119">Bu cmdlet 'in bir $True değerini (başarılı olursa), aksi takdirde $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="464c5-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="464c5-120">-UserID</span><span class="sxs-lookup"><span data-stu-id="464c5-120">-UserId</span></span>
<span data-ttu-id="464c5-121">Gruptan kaldırılacak kullanıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="464c5-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="464c5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="464c5-122">CommonParameters</span></span>
<span data-ttu-id="464c5-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="464c5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="464c5-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="464c5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="464c5-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="464c5-125">INPUTS</span></span>

### <span data-ttu-id="464c5-126">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="464c5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="464c5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="464c5-127">System.String</span></span>

### <span data-ttu-id="464c5-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="464c5-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="464c5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="464c5-129">OUTPUTS</span></span>

### <span data-ttu-id="464c5-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="464c5-130">System.Boolean</span></span>

## <span data-ttu-id="464c5-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="464c5-131">NOTES</span></span>

## <span data-ttu-id="464c5-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="464c5-132">RELATED LINKS</span></span>

[<span data-ttu-id="464c5-133">Add-Azapsananagementusertogroup</span><span class="sxs-lookup"><span data-stu-id="464c5-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="464c5-134">Get-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="464c5-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


