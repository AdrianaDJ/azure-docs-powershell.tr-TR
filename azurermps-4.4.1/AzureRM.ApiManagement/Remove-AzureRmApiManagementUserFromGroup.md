---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: 2867e8eec65de040a0da61a1af960abc9797bb18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763412"
---
# <span data-ttu-id="2297a-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="2297a-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="2297a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2297a-102">SYNOPSIS</span></span>
<span data-ttu-id="2297a-103">Kullanıcıyı gruptan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="2297a-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2297a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2297a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2297a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2297a-105">DESCRIPTION</span></span>
<span data-ttu-id="2297a-106">**Remove-Azurermapsananagementuserfromgroup** cmdlet 'i, bir kullanıcıyı var olan bir gruptan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="2297a-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="2297a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2297a-107">EXAMPLES</span></span>

### <span data-ttu-id="2297a-108">Örnek 1: gruptan kullanıcı kaldırma</span><span class="sxs-lookup"><span data-stu-id="2297a-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="2297a-109">Bu komut, bir kullanıcıyı gruptan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="2297a-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="2297a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2297a-110">PARAMETERS</span></span>

### <span data-ttu-id="2297a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2297a-111">-Context</span></span>
<span data-ttu-id="2297a-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2297a-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2297a-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2297a-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2297a-114">-GroupID</span><span class="sxs-lookup"><span data-stu-id="2297a-114">-GroupId</span></span>
<span data-ttu-id="2297a-115">Kullanıcının kaldırılacağı grubun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2297a-115">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="2297a-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2297a-116">-PassThru</span></span>
<span data-ttu-id="2297a-117">Bu cmdlet 'in bir $True değerini (başarılı olursa), aksi takdirde $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2297a-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="2297a-118">-UserID</span><span class="sxs-lookup"><span data-stu-id="2297a-118">-UserId</span></span>
<span data-ttu-id="2297a-119">Gruptan kaldırılacak kullanıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2297a-119">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="2297a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2297a-120">-DefaultProfile</span></span>
<span data-ttu-id="2297a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2297a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2297a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2297a-122">CommonParameters</span></span>
<span data-ttu-id="2297a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2297a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2297a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2297a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2297a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2297a-125">INPUTS</span></span>

## <span data-ttu-id="2297a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2297a-126">OUTPUTS</span></span>

### <span data-ttu-id="2297a-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2297a-127">System.Boolean</span></span>

## <span data-ttu-id="2297a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2297a-128">NOTES</span></span>

## <span data-ttu-id="2297a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2297a-129">RELATED LINKS</span></span>

[<span data-ttu-id="2297a-130">Add-Azurermapımanagementusertogroup</span><span class="sxs-lookup"><span data-stu-id="2297a-130">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="2297a-131">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="2297a-131">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


