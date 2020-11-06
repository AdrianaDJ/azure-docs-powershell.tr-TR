---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: bdcbac04d621319ac3837f1efaef52018e0f4eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595124"
---
# <span data-ttu-id="1a298-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="1a298-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="1a298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a298-102">SYNOPSIS</span></span>
<span data-ttu-id="1a298-103">Kullanıcıyı gruptan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="1a298-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a298-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a298-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a298-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a298-105">DESCRIPTION</span></span>
<span data-ttu-id="1a298-106">**Remove-Azurermapsananagementuserfromgroup** cmdlet 'i, bir kullanıcıyı var olan bir gruptan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="1a298-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="1a298-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a298-107">EXAMPLES</span></span>

### <span data-ttu-id="1a298-108">Örnek 1: gruptan kullanıcı kaldırma</span><span class="sxs-lookup"><span data-stu-id="1a298-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="1a298-109">Bu komut, bir kullanıcıyı gruptan çıkarır.</span><span class="sxs-lookup"><span data-stu-id="1a298-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="1a298-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a298-110">PARAMETERS</span></span>

### <span data-ttu-id="1a298-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1a298-111">-Context</span></span>
<span data-ttu-id="1a298-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a298-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="1a298-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1a298-113">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a298-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a298-114">-DefaultProfile</span></span>
<span data-ttu-id="1a298-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a298-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a298-116">-GroupID</span><span class="sxs-lookup"><span data-stu-id="1a298-116">-GroupId</span></span>
<span data-ttu-id="1a298-117">Kullanıcının kaldırılacağı grubun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a298-117">Specifies the ID of the group from which to remove a user.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a298-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1a298-118">-PassThru</span></span>
<span data-ttu-id="1a298-119">Bu cmdlet 'in bir $True değerini (başarılı olursa), aksi takdirde $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a298-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a298-120">-UserID</span><span class="sxs-lookup"><span data-stu-id="1a298-120">-UserId</span></span>
<span data-ttu-id="1a298-121">Gruptan kaldırılacak kullanıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a298-121">Specifies the ID of the user to remove from the group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a298-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a298-122">CommonParameters</span></span>
<span data-ttu-id="1a298-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a298-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a298-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a298-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a298-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a298-125">INPUTS</span></span>

### <span data-ttu-id="1a298-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1a298-126">None</span></span>
<span data-ttu-id="1a298-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1a298-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a298-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a298-128">OUTPUTS</span></span>

### <span data-ttu-id="1a298-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a298-129">System.Boolean</span></span>

## <span data-ttu-id="1a298-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a298-130">NOTES</span></span>

## <span data-ttu-id="1a298-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a298-131">RELATED LINKS</span></span>

[<span data-ttu-id="1a298-132">Add-Azurermapımanagementusertogroup</span><span class="sxs-lookup"><span data-stu-id="1a298-132">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="1a298-133">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="1a298-133">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


