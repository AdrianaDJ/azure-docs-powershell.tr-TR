---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 44cb5e9317c1806200a571dd6311e212e50a8c20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589526"
---
# <span data-ttu-id="17800-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="17800-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="17800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17800-102">SYNOPSIS</span></span>
<span data-ttu-id="17800-103">Bir abonelikteki ıothubs hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="17800-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17800-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17800-104">SYNTAX</span></span>

### <span data-ttu-id="17800-105">ListIotHubsByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17800-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17800-106">Getilebilirlik Ubbyname</span><span class="sxs-lookup"><span data-stu-id="17800-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17800-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="17800-107">DESCRIPTION</span></span>
<span data-ttu-id="17800-108">Bir abonelikteki ıothubs hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="17800-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="17800-109">Bir abonelikteki tüm IotHub örneklerini görüntüleyebilir ya da sonuçlarınızı kaynak grubuna veya belirli bir IotHub adına göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17800-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="17800-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17800-110">EXAMPLES</span></span>

### <span data-ttu-id="17800-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="17800-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="17800-112">Abonelikteki tüm ıothubleri alır.</span><span class="sxs-lookup"><span data-stu-id="17800-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="17800-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="17800-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="17800-114">Aboneliğindeki tüm ıothubleri "myresourcegroup" adlı resourcegroup 'a ait olarak alır.</span><span class="sxs-lookup"><span data-stu-id="17800-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="17800-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="17800-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="17800-116">"Myiothub" adındaki IotHub hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="17800-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="17800-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17800-117">PARAMETERS</span></span>

### <span data-ttu-id="17800-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17800-118">-DefaultProfile</span></span>
<span data-ttu-id="17800-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="17800-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17800-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="17800-120">-Name</span></span>
<span data-ttu-id="17800-121">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="17800-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17800-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17800-122">-ResourceGroupName</span></span>
<span data-ttu-id="17800-123">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17800-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17800-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17800-124">CommonParameters</span></span>
<span data-ttu-id="17800-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17800-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17800-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17800-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17800-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17800-127">INPUTS</span></span>

### <span data-ttu-id="17800-128">System. String</span><span class="sxs-lookup"><span data-stu-id="17800-128">System.String</span></span>

## <span data-ttu-id="17800-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17800-129">OUTPUTS</span></span>

### <span data-ttu-id="17800-130">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="17800-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="17800-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17800-131">NOTES</span></span>

## <span data-ttu-id="17800-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17800-132">RELATED LINKS</span></span>
