---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 890180c024a004652406e04530a7e3291def13ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594662"
---
# <span data-ttu-id="4d852-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="4d852-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="4d852-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d852-102">SYNOPSIS</span></span>
<span data-ttu-id="4d852-103">Bir abonelikteki ıothubs hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4d852-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d852-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d852-104">SYNTAX</span></span>

### <span data-ttu-id="4d852-105">ListIotHubsByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4d852-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d852-106">Getilebilirlik Ubbyname</span><span class="sxs-lookup"><span data-stu-id="4d852-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d852-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d852-107">DESCRIPTION</span></span>
<span data-ttu-id="4d852-108">Bir abonelikteki ıothubs hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4d852-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="4d852-109">Bir abonelikteki tüm IotHub örneklerini görüntüleyebilir ya da sonuçlarınızı kaynak grubuna veya belirli bir IotHub adına göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d852-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="4d852-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d852-110">EXAMPLES</span></span>

### <span data-ttu-id="4d852-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4d852-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="4d852-112">Abonelikteki tüm ıothubleri alır.</span><span class="sxs-lookup"><span data-stu-id="4d852-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="4d852-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4d852-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="4d852-114">Aboneliğindeki tüm ıothubleri "myresourcegroup" adlı resourcegroup 'a ait olarak alır.</span><span class="sxs-lookup"><span data-stu-id="4d852-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="4d852-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="4d852-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4d852-116">"Myiothub" adındaki IotHub hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4d852-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="4d852-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d852-117">PARAMETERS</span></span>

### <span data-ttu-id="4d852-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d852-118">-Name</span></span>
<span data-ttu-id="4d852-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="4d852-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="4d852-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d852-120">-ResourceGroupName</span></span>
<span data-ttu-id="4d852-121">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d852-121">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="4d852-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d852-122">-DefaultProfile</span></span>
<span data-ttu-id="4d852-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d852-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d852-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d852-124">CommonParameters</span></span>
<span data-ttu-id="4d852-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d852-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d852-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d852-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d852-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d852-127">INPUTS</span></span>

### <span data-ttu-id="4d852-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4d852-128">System.String</span></span>

## <span data-ttu-id="4d852-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d852-129">OUTPUTS</span></span>

### <span data-ttu-id="4d852-130">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="4d852-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="4d852-131">System. Koleksiyonlar. Generic. LIST \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotub, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="4d852-131">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="4d852-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d852-132">NOTES</span></span>

## <span data-ttu-id="4d852-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d852-133">RELATED LINKS</span></span>

