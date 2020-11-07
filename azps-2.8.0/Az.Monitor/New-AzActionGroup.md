---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 1377e1fe5f96754f4b20858cc1930039246bd8be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931881"
---
# <span data-ttu-id="65f9e-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="65f9e-101">New-AzActionGroup</span></span>

## <span data-ttu-id="65f9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="65f9e-103">Bellekte bir ActionGroup başvuru nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65f9e-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="65f9e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65f9e-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65f9e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="65f9e-105">DESCRIPTION</span></span>
<span data-ttu-id="65f9e-106">**New-AzActionGroup** cmdlet 'i bellekte bir eylem grubu başvuru nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65f9e-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="65f9e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65f9e-107">EXAMPLES</span></span>

### <span data-ttu-id="65f9e-108">Örnek 1: bellekte eylem grubu başvuru nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="65f9e-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="65f9e-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65f9e-109">PARAMETERS</span></span>

### <span data-ttu-id="65f9e-110">-Actiongroupıd</span><span class="sxs-lookup"><span data-stu-id="65f9e-110">-ActionGroupId</span></span>
<span data-ttu-id="65f9e-111">Eylem grubunun kimliği/adı.</span><span class="sxs-lookup"><span data-stu-id="65f9e-111">The Id/name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f9e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f9e-112">-DefaultProfile</span></span>
<span data-ttu-id="65f9e-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="65f9e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65f9e-114">-Web, Özellik</span><span class="sxs-lookup"><span data-stu-id="65f9e-114">-WebhookProperty</span></span>
<span data-ttu-id="65f9e-115">Eylem grubunun Web kancası özellikleri</span><span class="sxs-lookup"><span data-stu-id="65f9e-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f9e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f9e-116">CommonParameters</span></span>
<span data-ttu-id="65f9e-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65f9e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f9e-118">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="65f9e-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f9e-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65f9e-119">INPUTS</span></span>

### <span data-ttu-id="65f9e-120">System. String</span><span class="sxs-lookup"><span data-stu-id="65f9e-120">System.String</span></span>

### <span data-ttu-id="65f9e-121">System. Koleksiyonlar. Generic. Dictionary ' 2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85din</span><span class="sxs-lookup"><span data-stu-id="65f9e-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="65f9e-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65f9e-122">OUTPUTS</span></span>

### <span data-ttu-id="65f9e-123">Microsoft. Azure. Management. Monitor. Management. modeller. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="65f9e-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="65f9e-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65f9e-124">NOTES</span></span>

## <span data-ttu-id="65f9e-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65f9e-125">RELATED LINKS</span></span>

[<span data-ttu-id="65f9e-126">Set-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="65f9e-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="65f9e-127">Enable-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="65f9e-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="65f9e-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="65f9e-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="65f9e-129">Get-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="65f9e-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="65f9e-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="65f9e-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="65f9e-131">Yeni-Azactivilogalertcondition</span><span class="sxs-lookup"><span data-stu-id="65f9e-131">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

