---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: b0f4e67630a3a762fe78c9438c6ae39f948404c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764246"
---
# <span data-ttu-id="ee517-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ee517-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="ee517-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee517-102">SYNOPSIS</span></span>
<span data-ttu-id="ee517-103">Active Directory kullanıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="ee517-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee517-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee517-104">SYNTAX</span></span>

```
Remove-AzureRmADUser -UPNOrObjectId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee517-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee517-105">DESCRIPTION</span></span>
<span data-ttu-id="ee517-106">Active Directory kullanıcısını (iş/okul hesabı, ayrıca org-ID olarak da bilinir) siler.</span><span class="sxs-lookup"><span data-stu-id="ee517-106">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="ee517-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee517-107">EXAMPLES</span></span>

### <span data-ttu-id="ee517-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ee517-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ee517-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="ee517-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ee517-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee517-110">PARAMETERS</span></span>

### <span data-ttu-id="ee517-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ee517-111">-Force</span></span>
<span data-ttu-id="ee517-112">Belirtilmişse, Kullanıcı silme konusunda onay sormaz.</span><span class="sxs-lookup"><span data-stu-id="ee517-112">If specified, doesn't ask for confirmation for deleting user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee517-113">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="ee517-113">-UPNOrObjectId</span></span>
<span data-ttu-id="ee517-114">Silinecek kullanıcının Kullanıcı asıl adı veya ObjectID.</span><span class="sxs-lookup"><span data-stu-id="ee517-114">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="ee517-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee517-115">-Confirm</span></span>
<span data-ttu-id="ee517-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee517-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee517-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee517-117">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee517-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee517-118">-DefaultProfile</span></span>
<span data-ttu-id="ee517-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee517-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee517-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee517-120">CommonParameters</span></span>
<span data-ttu-id="ee517-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee517-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee517-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee517-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee517-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee517-123">INPUTS</span></span>

## <span data-ttu-id="ee517-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee517-124">OUTPUTS</span></span>

## <span data-ttu-id="ee517-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee517-125">NOTES</span></span>

## <span data-ttu-id="ee517-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee517-126">RELATED LINKS</span></span>

[<span data-ttu-id="ee517-127">Yeni-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ee517-127">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="ee517-128">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ee517-128">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="ee517-129">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ee517-129">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

