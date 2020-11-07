---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: 300c99926ae7f58a6bf53ba49f3b5b86f243e150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763594"
---
# <span data-ttu-id="736cb-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="736cb-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="736cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="736cb-102">SYNOPSIS</span></span>
<span data-ttu-id="736cb-103">Gruba bir kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="736cb-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="736cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="736cb-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="736cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="736cb-105">DESCRIPTION</span></span>
<span data-ttu-id="736cb-106">**Add-Azurermapımanagementusertogroup** cmdlet 'i bir gruba kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="736cb-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="736cb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="736cb-107">EXAMPLES</span></span>

### <span data-ttu-id="736cb-108">Örnek 1: gruba kullanıcı ekleme</span><span class="sxs-lookup"><span data-stu-id="736cb-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="736cb-109">Bu komut mevcut bir gruba varolan bir kullanıcıyı ekler.</span><span class="sxs-lookup"><span data-stu-id="736cb-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="736cb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="736cb-110">PARAMETERS</span></span>

### <span data-ttu-id="736cb-111">-Context</span><span class="sxs-lookup"><span data-stu-id="736cb-111">-Context</span></span>
<span data-ttu-id="736cb-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="736cb-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="736cb-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="736cb-113">This parameter is required.</span></span>

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

### <span data-ttu-id="736cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="736cb-114">-DefaultProfile</span></span>
<span data-ttu-id="736cb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="736cb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="736cb-116">-GroupID</span><span class="sxs-lookup"><span data-stu-id="736cb-116">-GroupId</span></span>
<span data-ttu-id="736cb-117">Grup KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="736cb-117">Specifies the group ID.</span></span>
<span data-ttu-id="736cb-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="736cb-118">This parameter is required.</span></span>

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

### <span data-ttu-id="736cb-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="736cb-119">-PassThru</span></span>
<span data-ttu-id="736cb-120">geçiş</span><span class="sxs-lookup"><span data-stu-id="736cb-120">passthru</span></span>

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

### <span data-ttu-id="736cb-121">-UserID</span><span class="sxs-lookup"><span data-stu-id="736cb-121">-UserId</span></span>
<span data-ttu-id="736cb-122">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="736cb-122">Specifies the user ID.</span></span>
<span data-ttu-id="736cb-123">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="736cb-123">This parameter is required.</span></span>

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

### <span data-ttu-id="736cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="736cb-124">CommonParameters</span></span>
<span data-ttu-id="736cb-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="736cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="736cb-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="736cb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="736cb-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="736cb-127">INPUTS</span></span>

### <span data-ttu-id="736cb-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="736cb-128">None</span></span>
<span data-ttu-id="736cb-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="736cb-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="736cb-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="736cb-130">OUTPUTS</span></span>

### <span data-ttu-id="736cb-131">Boole</span><span class="sxs-lookup"><span data-stu-id="736cb-131">Boolean</span></span>

## <span data-ttu-id="736cb-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="736cb-132">NOTES</span></span>

## <span data-ttu-id="736cb-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="736cb-133">RELATED LINKS</span></span>

[<span data-ttu-id="736cb-134">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="736cb-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="736cb-135">Remove-Azurermapımanagementuserfromgroup</span><span class="sxs-lookup"><span data-stu-id="736cb-135">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


