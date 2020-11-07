---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 1076ff16005665aa81e4775507a236fe62bb0965
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936703"
---
# <span data-ttu-id="12d56-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="12d56-101">Get-AzIotHub</span></span>

## <span data-ttu-id="12d56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12d56-102">SYNOPSIS</span></span>
<span data-ttu-id="12d56-103">Bir abonelikteki ıothubs hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="12d56-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="12d56-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12d56-104">SYNTAX</span></span>

### <span data-ttu-id="12d56-105">ListIotHubsByResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="12d56-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12d56-106">Getilebilirlik Ubbyname</span><span class="sxs-lookup"><span data-stu-id="12d56-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12d56-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="12d56-107">DESCRIPTION</span></span>
<span data-ttu-id="12d56-108">Bir abonelikteki ıothubs hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="12d56-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="12d56-109">Bir abonelikteki tüm IotHub örneklerini görüntüleyebilir ya da sonuçlarınızı kaynak grubuna veya belirli bir IotHub adına göre filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12d56-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="12d56-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12d56-110">EXAMPLES</span></span>

### <span data-ttu-id="12d56-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="12d56-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="12d56-112">Abonelikteki tüm ıothubleri alır.</span><span class="sxs-lookup"><span data-stu-id="12d56-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="12d56-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="12d56-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="12d56-114">Aboneliğindeki tüm ıothubleri "myresourcegroup" adlı resourcegroup 'a ait olarak alır.</span><span class="sxs-lookup"><span data-stu-id="12d56-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="12d56-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="12d56-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="12d56-116">"Myiothub" adındaki IotHub hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="12d56-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="12d56-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12d56-117">PARAMETERS</span></span>

### <span data-ttu-id="12d56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d56-118">-DefaultProfile</span></span>
<span data-ttu-id="12d56-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="12d56-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12d56-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="12d56-120">-Name</span></span>
<span data-ttu-id="12d56-121">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="12d56-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="12d56-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d56-122">-ResourceGroupName</span></span>
<span data-ttu-id="12d56-123">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="12d56-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="12d56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d56-124">CommonParameters</span></span>
<span data-ttu-id="12d56-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12d56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d56-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d56-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d56-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12d56-127">INPUTS</span></span>

### <span data-ttu-id="12d56-128">System. String</span><span class="sxs-lookup"><span data-stu-id="12d56-128">System.String</span></span>

## <span data-ttu-id="12d56-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12d56-129">OUTPUTS</span></span>

### <span data-ttu-id="12d56-130">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="12d56-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="12d56-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12d56-131">NOTES</span></span>

## <span data-ttu-id="12d56-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12d56-132">RELATED LINKS</span></span>
