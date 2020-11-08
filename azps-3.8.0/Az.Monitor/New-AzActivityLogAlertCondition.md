---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 4932445406e19cbc05f5e2680871a03ae6f40f60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098463"
---
# <span data-ttu-id="7902d-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="7902d-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="7902d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7902d-102">SYNOPSIS</span></span>
<span data-ttu-id="7902d-103">Bellekte yeni bir etkinlik günlüğü uyarı koşulu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7902d-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="7902d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7902d-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7902d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7902d-105">DESCRIPTION</span></span>
<span data-ttu-id="7902d-106">**New-Azactivilogalertcondition** cmdlet 'i bellekte yeni etkinlik günlüğü uyarı koşulu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7902d-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="7902d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7902d-107">EXAMPLES</span></span>

### <span data-ttu-id="7902d-108">Örnek 1: bellekte yeni bir etkinlik günlüğü uyarı koşulu nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7902d-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="7902d-109">Bu komut, bellekte yeni bir etkinlik günlüğü uyarı koşulu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7902d-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="7902d-110">**Not** : Bu cmdlet, parametre olarak geçirilen bu nesnelerden en az biriyle Set-AzActivityLogAlert ile kullanıldığında, alanı "Category" değerine eşit olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7902d-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="7902d-111">Aksi takdirde, arka uç 400 (BadRequest) ile yanıt verir.</span><span class="sxs-lookup"><span data-stu-id="7902d-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="7902d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7902d-112">PARAMETERS</span></span>

### <span data-ttu-id="7902d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7902d-113">-DefaultProfile</span></span>
<span data-ttu-id="7902d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7902d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7902d-115">-Eşittir</span><span class="sxs-lookup"><span data-stu-id="7902d-115">-Equal</span></span>
<span data-ttu-id="7902d-116">Yaprak koşulunun eşittir özelliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7902d-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="7902d-117">-Alan</span><span class="sxs-lookup"><span data-stu-id="7902d-117">-Field</span></span>
<span data-ttu-id="7902d-118">Koşul için alanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="7902d-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="7902d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7902d-119">CommonParameters</span></span>
<span data-ttu-id="7902d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7902d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7902d-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7902d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7902d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7902d-122">INPUTS</span></span>

### <span data-ttu-id="7902d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7902d-123">System.String</span></span>

## <span data-ttu-id="7902d-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7902d-124">OUTPUTS</span></span>

### <span data-ttu-id="7902d-125">Microsoft. Azure. Management. Monitor. Management. modeller. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="7902d-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="7902d-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7902d-126">NOTES</span></span>

## <span data-ttu-id="7902d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7902d-127">RELATED LINKS</span></span>

[<span data-ttu-id="7902d-128">Set-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="7902d-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="7902d-129">Enable-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="7902d-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="7902d-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7902d-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="7902d-131">Get-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="7902d-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="7902d-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="7902d-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="7902d-133">Yeni-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="7902d-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)