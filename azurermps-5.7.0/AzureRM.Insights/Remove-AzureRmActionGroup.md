---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 1d4a5365ac2112364a544eb2481a3193f23519c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592495"
---
# <span data-ttu-id="0b1db-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="0b1db-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="0b1db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b1db-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1db-103">Eylem grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0b1db-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b1db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b1db-104">SYNTAX</span></span>

### <span data-ttu-id="0b1db-105">ByPropertyName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b1db-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b1db-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0b1db-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b1db-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0b1db-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b1db-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b1db-108">DESCRIPTION</span></span>
<span data-ttu-id="0b1db-109">**Remove-AzureRmActionGroup** cmdlet 'i bir eylem grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0b1db-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="0b1db-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b1db-110">EXAMPLES</span></span>

### <span data-ttu-id="0b1db-111">Örnek 1: Eylem grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="0b1db-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="0b1db-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b1db-112">PARAMETERS</span></span>

### <span data-ttu-id="0b1db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1db-113">-DefaultProfile</span></span>
<span data-ttu-id="0b1db-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0b1db-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b1db-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b1db-115">-InputObject</span></span>
<span data-ttu-id="0b1db-116">Grup kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="0b1db-116">The action group resourc</span></span>

```yaml
Type: PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b1db-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b1db-117">-Name</span></span>
<span data-ttu-id="0b1db-118">Eylem grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0b1db-118">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b1db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b1db-119">-ResourceGroupName</span></span>
<span data-ttu-id="0b1db-120">Kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="0b1db-120">The resource group nam</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b1db-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0b1db-121">-ResourceId</span></span>
<span data-ttu-id="0b1db-122">Kaynak ı</span><span class="sxs-lookup"><span data-stu-id="0b1db-122">The resource i</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b1db-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b1db-123">-Confirm</span></span>
<span data-ttu-id="0b1db-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b1db-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b1db-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b1db-125">-WhatIf</span></span>
<span data-ttu-id="0b1db-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b1db-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b1db-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b1db-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b1db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1db-128">CommonParameters</span></span>
<span data-ttu-id="0b1db-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b1db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1db-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b1db-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1db-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b1db-131">INPUTS</span></span>

### <span data-ttu-id="0b1db-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0b1db-132">None</span></span>
<span data-ttu-id="0b1db-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0b1db-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b1db-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b1db-134">OUTPUTS</span></span>

### <span data-ttu-id="0b1db-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0b1db-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0b1db-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b1db-136">NOTES</span></span>

## <span data-ttu-id="0b1db-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b1db-137">RELATED LINKS</span></span>

<span data-ttu-id="0b1db-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Yeni-Azurermactiongroupahize](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="0b1db-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
