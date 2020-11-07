---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 01b8283277c1d9592adbd8edfe6b883a4451ded9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763249"
---
# <span data-ttu-id="386da-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="386da-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="386da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="386da-102">SYNOPSIS</span></span>
<span data-ttu-id="386da-103">Geçerli bağlamda varsayılan ayarlar</span><span class="sxs-lookup"><span data-stu-id="386da-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="386da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="386da-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="386da-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="386da-105">DESCRIPTION</span></span>
<span data-ttu-id="386da-106">Set-AzureRmDefault cmdlet 'i geçerli içerikte Varsayılanları ekler veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="386da-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="386da-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="386da-107">EXAMPLES</span></span>

### <span data-ttu-id="386da-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="386da-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="386da-109">Bu komut, varsayılan kaynak grubunu Kullanıcı tarafından belirtilen kaynak grubuyla ayarlar.</span><span class="sxs-lookup"><span data-stu-id="386da-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="386da-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="386da-110">PARAMETERS</span></span>

### <span data-ttu-id="386da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386da-111">-DefaultProfile</span></span>
<span data-ttu-id="386da-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="386da-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="386da-113">-Force</span><span class="sxs-lookup"><span data-stu-id="386da-113">-Force</span></span>
<span data-ttu-id="386da-114">Belirtilen varsayılan yoksa yeni bir kaynak grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="386da-114">Create a new resource group if specified default does not exist</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="386da-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="386da-115">-ResourceGroupName</span></span>
<span data-ttu-id="386da-116">Varsayılan olarak ayarlanan kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="386da-116">Name of the resource group being set as default</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="386da-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="386da-117">-Confirm</span></span>
<span data-ttu-id="386da-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="386da-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="386da-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="386da-119">-WhatIf</span></span>
<span data-ttu-id="386da-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="386da-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="386da-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="386da-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="386da-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386da-122">CommonParameters</span></span>
<span data-ttu-id="386da-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="386da-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="386da-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="386da-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386da-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="386da-125">INPUTS</span></span>

### <span data-ttu-id="386da-126">System. String</span><span class="sxs-lookup"><span data-stu-id="386da-126">System.String</span></span>

## <span data-ttu-id="386da-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="386da-127">OUTPUTS</span></span>

### <span data-ttu-id="386da-128">Microsoft. Azure. Management. Internal. resources. modeller. ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="386da-128">Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroup</span></span>

## <span data-ttu-id="386da-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="386da-129">NOTES</span></span>

## <span data-ttu-id="386da-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="386da-130">RELATED LINKS</span></span>

