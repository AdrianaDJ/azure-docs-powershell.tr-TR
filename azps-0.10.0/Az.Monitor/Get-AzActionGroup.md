---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: ca4229f5f882b1065c6f39b8c162bb91b90b835d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935754"
---
# <span data-ttu-id="72db8-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="72db8-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="72db8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72db8-102">SYNOPSIS</span></span>
<span data-ttu-id="72db8-103">Eylem gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="72db8-103">Gets action group(s).</span></span>

## <span data-ttu-id="72db8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72db8-104">SYNTAX</span></span>

### <span data-ttu-id="72db8-105">BySubscriptionOrResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="72db8-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72db8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="72db8-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72db8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="72db8-107">DESCRIPTION</span></span>
<span data-ttu-id="72db8-108">**Get-AzActionGroup** cmdlet 'i bir veya daha fazla eylem grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="72db8-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="72db8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72db8-109">EXAMPLES</span></span>

### <span data-ttu-id="72db8-110">Örnek 1: abonelik KIMLIĞIYLE bir eylem grubu alma</span><span class="sxs-lookup"><span data-stu-id="72db8-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="72db8-111">Bu komut geçerli aboneliğin tüm eylem gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="72db8-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="72db8-112">Örnek 2: verilen kaynak grubunun eylem gruplarını alma</span><span class="sxs-lookup"><span data-stu-id="72db8-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="72db8-113">Bu komut, verilen kaynak grubunun eylem gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="72db8-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="72db8-114">Örnek 3: bir eylem grubu edinin.</span><span class="sxs-lookup"><span data-stu-id="72db8-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="72db8-115">Bu komut, bir (tek öğe içeren bir liste) eylem grubuyla listelenir.</span><span class="sxs-lookup"><span data-stu-id="72db8-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="72db8-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72db8-116">PARAMETERS</span></span>

### <span data-ttu-id="72db8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72db8-117">-DefaultProfile</span></span>
<span data-ttu-id="72db8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="72db8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72db8-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="72db8-119">-Name</span></span>
<span data-ttu-id="72db8-120">Eylem grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="72db8-120">The name of the action group.</span></span>

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

### <span data-ttu-id="72db8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72db8-121">-ResourceGroupName</span></span>
<span data-ttu-id="72db8-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="72db8-122">The resource group name</span></span>

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

### <span data-ttu-id="72db8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72db8-123">CommonParameters</span></span>
<span data-ttu-id="72db8-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72db8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72db8-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="72db8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72db8-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72db8-126">INPUTS</span></span>

### <span data-ttu-id="72db8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="72db8-127">System.String</span></span>

## <span data-ttu-id="72db8-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72db8-128">OUTPUTS</span></span>

### <span data-ttu-id="72db8-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="72db8-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="72db8-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72db8-130">NOTES</span></span>

## <span data-ttu-id="72db8-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72db8-131">RELATED LINKS</span></span>

<span data-ttu-id="72db8-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [Yeni-Azactiongroupahize](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="72db8-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
