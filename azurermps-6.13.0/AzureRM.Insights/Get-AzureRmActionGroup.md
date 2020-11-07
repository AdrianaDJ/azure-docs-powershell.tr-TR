---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 002847ae580e3e3c5d5b44e05ebc1633e4e1574b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762723"
---
# <span data-ttu-id="a7fec-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a7fec-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="a7fec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7fec-102">SYNOPSIS</span></span>
<span data-ttu-id="a7fec-103">Eylem gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="a7fec-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7fec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7fec-104">SYNTAX</span></span>

### <span data-ttu-id="a7fec-105">BySubscriptionOrResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7fec-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7fec-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a7fec-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7fec-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7fec-107">DESCRIPTION</span></span>
<span data-ttu-id="a7fec-108">**Get-AzureRmActionGroup** cmdlet 'i bir veya daha fazla eylem grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="a7fec-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="a7fec-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7fec-109">EXAMPLES</span></span>

### <span data-ttu-id="a7fec-110">Örnek 1: abonelik KIMLIĞIYLE bir eylem grubu alma</span><span class="sxs-lookup"><span data-stu-id="a7fec-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="a7fec-111">Bu komut geçerli aboneliğin tüm eylem gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="a7fec-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="a7fec-112">Örnek 2: verilen kaynak grubunun eylem gruplarını alma</span><span class="sxs-lookup"><span data-stu-id="a7fec-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="a7fec-113">Bu komut, verilen kaynak grubunun eylem gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="a7fec-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="a7fec-114">Örnek 3: bir eylem grubu edinin.</span><span class="sxs-lookup"><span data-stu-id="a7fec-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="a7fec-115">Bu komut, bir (tek öğe içeren bir liste) eylem grubuyla listelenir.</span><span class="sxs-lookup"><span data-stu-id="a7fec-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="a7fec-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7fec-116">PARAMETERS</span></span>

### <span data-ttu-id="a7fec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7fec-117">-DefaultProfile</span></span>
<span data-ttu-id="a7fec-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a7fec-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7fec-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7fec-119">-Name</span></span>
<span data-ttu-id="a7fec-120">Eylem grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a7fec-120">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7fec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7fec-121">-ResourceGroupName</span></span>
<span data-ttu-id="a7fec-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a7fec-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7fec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7fec-123">CommonParameters</span></span>
<span data-ttu-id="a7fec-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7fec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7fec-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7fec-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7fec-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7fec-126">INPUTS</span></span>

### <span data-ttu-id="a7fec-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a7fec-127">System.String</span></span>

## <span data-ttu-id="a7fec-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7fec-128">OUTPUTS</span></span>

### <span data-ttu-id="a7fec-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="a7fec-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="a7fec-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7fec-130">NOTES</span></span>

## <span data-ttu-id="a7fec-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7fec-131">RELATED LINKS</span></span>

<span data-ttu-id="a7fec-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Yeni-Azurermactiongroupahize](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="a7fec-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
