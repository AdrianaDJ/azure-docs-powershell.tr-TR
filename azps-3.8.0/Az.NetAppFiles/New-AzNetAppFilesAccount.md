---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 70bfdb4f590c855199bb8bbd14db4e92809b48f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937323"
---
# <span data-ttu-id="0613d-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0613d-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="0613d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0613d-102">SYNOPSIS</span></span>
<span data-ttu-id="0613d-103">Yeni bir Azure NetApp dosyaları (ANF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0613d-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="0613d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0613d-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0613d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0613d-105">DESCRIPTION</span></span>
<span data-ttu-id="0613d-106">**New-AzNetAppFilesAccount** cmdlet 'ı BIR ANF hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0613d-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="0613d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0613d-107">EXAMPLES</span></span>

### <span data-ttu-id="0613d-108">Örnek 1: ANF hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="0613d-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="0613d-109">Bu komut, "MyAnfAccount" yeni ANF hesabını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0613d-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="0613d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0613d-110">PARAMETERS</span></span>

### <span data-ttu-id="0613d-111">-Activedizinler</span><span class="sxs-lookup"><span data-stu-id="0613d-111">-ActiveDirectories</span></span>
<span data-ttu-id="0613d-112">Active Directory 'yi temsil eden bir Hashtable dizisi</span><span class="sxs-lookup"><span data-stu-id="0613d-112">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0613d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0613d-113">-DefaultProfile</span></span>
<span data-ttu-id="0613d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0613d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0613d-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="0613d-115">-Location</span></span>
<span data-ttu-id="0613d-116">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="0613d-116">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0613d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0613d-117">-Name</span></span>
<span data-ttu-id="0613d-118">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="0613d-118">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0613d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0613d-119">-ResourceGroupName</span></span>
<span data-ttu-id="0613d-120">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="0613d-120">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0613d-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="0613d-121">-Tag</span></span>
<span data-ttu-id="0613d-122">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="0613d-122">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0613d-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="0613d-123">-Confirm</span></span>
<span data-ttu-id="0613d-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0613d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0613d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0613d-125">-WhatIf</span></span>
<span data-ttu-id="0613d-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0613d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0613d-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0613d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0613d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0613d-128">CommonParameters</span></span>
<span data-ttu-id="0613d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0613d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0613d-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0613d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0613d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0613d-131">INPUTS</span></span>

### <span data-ttu-id="0613d-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0613d-132">None</span></span>

## <span data-ttu-id="0613d-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0613d-133">OUTPUTS</span></span>

### <span data-ttu-id="0613d-134">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0613d-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="0613d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0613d-135">NOTES</span></span>

## <span data-ttu-id="0613d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0613d-136">RELATED LINKS</span></span>
