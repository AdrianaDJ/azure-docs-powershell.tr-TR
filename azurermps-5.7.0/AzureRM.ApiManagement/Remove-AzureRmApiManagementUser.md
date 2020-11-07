---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 5d657610ddce1c0397a5f9e8c11b832b3fcd472b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765124"
---
# <span data-ttu-id="2be45-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2be45-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="2be45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2be45-102">SYNOPSIS</span></span>
<span data-ttu-id="2be45-103">Var olan kullanıcıyı siler.</span><span class="sxs-lookup"><span data-stu-id="2be45-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2be45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2be45-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2be45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2be45-105">DESCRIPTION</span></span>
<span data-ttu-id="2be45-106">**Remove-Azurermapsananagementuser** cmdlet 'i var olan kullanıcıyı siler.</span><span class="sxs-lookup"><span data-stu-id="2be45-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="2be45-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2be45-107">EXAMPLES</span></span>

### <span data-ttu-id="2be45-108">Örnek 1: Kullanıcı silme</span><span class="sxs-lookup"><span data-stu-id="2be45-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="2be45-109">Bu komut mevcut bir kullanıcıyı siler.</span><span class="sxs-lookup"><span data-stu-id="2be45-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="2be45-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2be45-110">PARAMETERS</span></span>

### <span data-ttu-id="2be45-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2be45-111">-Context</span></span>
<span data-ttu-id="2be45-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2be45-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2be45-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2be45-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2be45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be45-114">-DefaultProfile</span></span>
<span data-ttu-id="2be45-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2be45-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2be45-116">-Deleteabonelikleri</span><span class="sxs-lookup"><span data-stu-id="2be45-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="2be45-117">Ürüne aboneliklerin silineceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2be45-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="2be45-118">Bu parametre belirtilmemişse ve bir abonelik varsa, bu cmdlet bir istisna oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2be45-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="2be45-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2be45-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="2be45-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2be45-120">-PassThru</span></span>
<span data-ttu-id="2be45-121">Bu cmdlet 'in bir $Ture değerini (başarılı olursa), aksi takdirde $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2be45-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="2be45-122">-UserID</span><span class="sxs-lookup"><span data-stu-id="2be45-122">-UserId</span></span>
<span data-ttu-id="2be45-123">Kaldırılacak kullanıcının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2be45-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="2be45-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="2be45-124">-Confirm</span></span>
<span data-ttu-id="2be45-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2be45-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be45-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2be45-126">-WhatIf</span></span>
<span data-ttu-id="2be45-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2be45-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2be45-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2be45-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be45-129">CommonParameters</span></span>
<span data-ttu-id="2be45-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2be45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be45-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2be45-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be45-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2be45-132">INPUTS</span></span>

### <span data-ttu-id="2be45-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2be45-133">None</span></span>
<span data-ttu-id="2be45-134">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2be45-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2be45-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2be45-135">OUTPUTS</span></span>

### <span data-ttu-id="2be45-136">Boole</span><span class="sxs-lookup"><span data-stu-id="2be45-136">Boolean</span></span>

## <span data-ttu-id="2be45-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2be45-137">NOTES</span></span>

## <span data-ttu-id="2be45-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2be45-138">RELATED LINKS</span></span>

[<span data-ttu-id="2be45-139">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="2be45-139">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="2be45-140">Yeni-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="2be45-140">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="2be45-141">Set-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="2be45-141">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


