---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319498"
---
# <span data-ttu-id="aaf0e-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="aaf0e-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="aaf0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaf0e-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf0e-103">Belirtilen projedeki tüm sürücüler için BitLocker anahtarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="aaf0e-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="aaf0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aaf0e-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="aaf0e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aaf0e-105">DESCRIPTION</span></span>
<span data-ttu-id="aaf0e-106">Belirtilen projedeki tüm sürücüler için BitLocker anahtarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="aaf0e-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="aaf0e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aaf0e-107">EXAMPLES</span></span>

### <span data-ttu-id="aaf0e-108">Örnek 1: belirtilen ımportexport işinde tüm BitLocker anahtarlarını Listele</span><span class="sxs-lookup"><span data-stu-id="aaf0e-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="aaf0e-109">Bu cmdlet belirtilen ımportexport işinde tüm BitLocker anahtarlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="aaf0e-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="aaf0e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aaf0e-110">PARAMETERS</span></span>

### <span data-ttu-id="aaf0e-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="aaf0e-111">-AcceptLanguage</span></span>
<span data-ttu-id="aaf0e-112">Yanıtın tercih ettiği dili belirtir.</span><span class="sxs-lookup"><span data-stu-id="aaf0e-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf0e-113">-DefaultProfile</span></span>
<span data-ttu-id="aaf0e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aaf0e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaf0e-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="aaf0e-115">-JobName</span></span>
<span data-ttu-id="aaf0e-116">İçeri/dışarı aktarma işinin adı.</span><span class="sxs-lookup"><span data-stu-id="aaf0e-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="aaf0e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf0e-117">-ResourceGroupName</span></span>
<span data-ttu-id="aaf0e-118">Kaynak grubu adı, kullanıcı aboneliği içinde kaynak grubunu benzersiz olarak tanımlar.</span><span class="sxs-lookup"><span data-stu-id="aaf0e-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="aaf0e-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="aaf0e-119">-SubscriptionId</span></span>
<span data-ttu-id="aaf0e-120">Azure kullanıcısına ait abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="aaf0e-120">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf0e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf0e-121">CommonParameters</span></span>
<span data-ttu-id="aaf0e-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aaf0e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf0e-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aaf0e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf0e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aaf0e-124">INPUTS</span></span>

## <span data-ttu-id="aaf0e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aaf0e-125">OUTPUTS</span></span>

### <span data-ttu-id="aaf0e-126">Microsoft. Azure. PowerShell. cmdlet. ımportexport. modeller. Api20161101. ıdrivebitlockerkey</span><span class="sxs-lookup"><span data-stu-id="aaf0e-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="aaf0e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aaf0e-127">NOTES</span></span>

<span data-ttu-id="aaf0e-128">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="aaf0e-128">ALIASES</span></span>

## <span data-ttu-id="aaf0e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aaf0e-129">RELATED LINKS</span></span>

