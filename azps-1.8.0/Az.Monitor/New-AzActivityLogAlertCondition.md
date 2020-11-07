---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 52788c012a7da6013e58df924d1eda0a3aa5afcb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915636"
---
# <span data-ttu-id="22c84-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="22c84-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="22c84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22c84-102">SYNOPSIS</span></span>
<span data-ttu-id="22c84-103">Bellekte yeni bir etkinlik günlüğü uyarı koşulu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="22c84-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="22c84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22c84-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22c84-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22c84-105">DESCRIPTION</span></span>
<span data-ttu-id="22c84-106">**New-Azactivilogalertcondition** cmdlet 'i bellekte yeni etkinlik günlüğü uyarı koşulu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="22c84-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="22c84-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22c84-107">EXAMPLES</span></span>

### <span data-ttu-id="22c84-108">Örnek 1: bellekte yeni bir etkinlik günlüğü uyarı koşulu nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="22c84-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="22c84-109">Bu komut, bellekte yeni bir etkinlik günlüğü uyarı koşulu nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="22c84-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="22c84-110">**Not** : Bu cmdlet, parametre olarak geçirilen bu nesnelerden en az biriyle Set-AzActivityLogAlert ile kullanıldığında, alanı "Category" değerine eşit olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="22c84-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="22c84-111">Aksi takdirde, arka uç 400 (BadRequest) ile yanıt verir.</span><span class="sxs-lookup"><span data-stu-id="22c84-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="22c84-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22c84-112">PARAMETERS</span></span>

### <span data-ttu-id="22c84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c84-113">-DefaultProfile</span></span>
<span data-ttu-id="22c84-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="22c84-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22c84-115">-Eşittir</span><span class="sxs-lookup"><span data-stu-id="22c84-115">-Equal</span></span>
<span data-ttu-id="22c84-116">Yaprak koşulunun eşittir özelliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c84-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="22c84-117">-Alan</span><span class="sxs-lookup"><span data-stu-id="22c84-117">-Field</span></span>
<span data-ttu-id="22c84-118">Koşul için alanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="22c84-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="22c84-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c84-119">CommonParameters</span></span>
<span data-ttu-id="22c84-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22c84-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c84-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22c84-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c84-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22c84-122">INPUTS</span></span>

### <span data-ttu-id="22c84-123">System. String</span><span class="sxs-lookup"><span data-stu-id="22c84-123">System.String</span></span>

## <span data-ttu-id="22c84-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22c84-124">OUTPUTS</span></span>

### <span data-ttu-id="22c84-125">Microsoft. Azure. Management. Monitor. Management. modeller. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="22c84-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="22c84-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22c84-126">NOTES</span></span>

## <span data-ttu-id="22c84-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22c84-127">RELATED LINKS</span></span>

[<span data-ttu-id="22c84-128">Set-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="22c84-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="22c84-129">Enable-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="22c84-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="22c84-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="22c84-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="22c84-131">Get-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="22c84-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="22c84-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="22c84-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="22c84-133">Yeni-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="22c84-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)