---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 0f82c80e9f06abd5a2189bbee665de58ee6a3528
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108318"
---
# <span data-ttu-id="273c7-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="273c7-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="273c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="273c7-102">SYNOPSIS</span></span>
<span data-ttu-id="273c7-103">Windows sanal masaüstü kayıt bilgilerini edinin.</span><span class="sxs-lookup"><span data-stu-id="273c7-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="273c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="273c7-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="273c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="273c7-105">DESCRIPTION</span></span>
<span data-ttu-id="273c7-106">Windows sanal masaüstü kayıt bilgilerini edinin.</span><span class="sxs-lookup"><span data-stu-id="273c7-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="273c7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="273c7-107">EXAMPLES</span></span>

### <span data-ttu-id="273c7-108">Örnek 1: Windows sanal masaüstü kayıt belirtecini alma</span><span class="sxs-lookup"><span data-stu-id="273c7-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="273c7-109">Bu komut, bir konak havuzunda Windows sanal masaüstü kayıt belirtecini alır.</span><span class="sxs-lookup"><span data-stu-id="273c7-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="273c7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="273c7-110">PARAMETERS</span></span>

### <span data-ttu-id="273c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273c7-111">-DefaultProfile</span></span>
<span data-ttu-id="273c7-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="273c7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273c7-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="273c7-113">-HostPoolName</span></span>
<span data-ttu-id="273c7-114">Konak havuzu adı</span><span class="sxs-lookup"><span data-stu-id="273c7-114">Host Pool Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="273c7-115">-ResourceGroupName</span></span>
<span data-ttu-id="273c7-116">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="273c7-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273c7-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="273c7-117">-SubscriptionId</span></span>
<span data-ttu-id="273c7-118">Abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="273c7-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273c7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273c7-119">CommonParameters</span></span>
<span data-ttu-id="273c7-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="273c7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273c7-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="273c7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273c7-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="273c7-122">INPUTS</span></span>

## <span data-ttu-id="273c7-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="273c7-123">OUTPUTS</span></span>

### <span data-ttu-id="273c7-124">Microsoft. Azure. PowerShell. cmdlet. DesktopVirtualization. modeller. Api20191210Preview. RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="273c7-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.RegistrationInfo</span></span>

## <span data-ttu-id="273c7-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="273c7-125">NOTES</span></span>

<span data-ttu-id="273c7-126">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="273c7-126">ALIASES</span></span>

## <span data-ttu-id="273c7-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="273c7-127">RELATED LINKS</span></span>

